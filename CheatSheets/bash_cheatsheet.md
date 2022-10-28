---
title: BASH CheatSheet
description: The most commonly used bash commands are given here.
created: 2022-10-23
---

## Table of Contents

- [BASH CheatSheet for Developers](#bash-cheatsheet-for-developers)
  - [Commands](#commands)
    - [`tr command`](#tr-command)
  - [One Liners](#one-liners)
    - [`Block Bad IPs`](#block-bad-ips)
  - [If Statements](#if-statements)
    - [`Check if args are passed`](#check-if-args-are-passed)
    - [`Check if required variables exist`](#check-if-required-variables-exist)
    - [`Check if environment variables exists`](#check-if-environment-variables-exists)
  - [While Loops](#while-loops)
    - [`Run process for 5 Seconds`](#run-process-for-5-seconds)
    - [`Run until state changes within ttl`](#run-until-state-changes-within-ttl)
  - [for Loops](#for-loops)
    - [`Upload all docker image`](#upload-all-docker-image)
  - [Functions](#functions)
  - [Redirecting Outputs](#redirecting-outputs)
    - [`Stdout, Stderr`](#stdout-stderr)
  - [Manipulating Text](#manipulating-text)
    - [`Remove first 3 characters`](#remove-first-3-characters)
    - [`Only show last 3 characters`](#only-show-last-3-characters)

# BASH CheatSheet for Developers

## Commands

### `tr command`

> ___Remove whitespace:___

```
$ echo 'foo - bar' | tr -d '[:space:]'
foo-bar
```

> ___Convert to uppercase:___

```
$ echo 'HeLLo' | tr '[:lower:]' '[:upper:]'
HELLO
```

**[🔼Back to Top](#table-of-contents)**

## One Liners

### `Block Bad IPs`

> Use iptables to block all bad ip addresses:

```
$ cat /var/log/maillog | grep 'lost connection after AUTH from unknown' | tail -n 5
May 10 11:19:49 srv4 postfix/smtpd[1486]: lost connection after AUTH from unknown[185.36.81.145]
May 10 11:21:41 srv4 postfix/smtpd[1762]: lost connection after AUTH from unknown[185.36.81.164]
May 10 11:21:56 srv4 postfix/smtpd[1762]: lost connection after AUTH from unknown[175.139.231.129]
May 10 11:23:51 srv4 postfix/smtpd[1838]: lost connection after AUTH from unknown[185.211.245.170]
May 10 11:24:02 srv4 postfix/smtpd[1838]: lost connection after AUTH from unknown[185.211.245.170]
```

> Get the data to show only IPs:

```
cat /var/log/maillog | grep 'lost connection after AUTH from unknown' | cut -d'[' -f3 | cut -d ']' -f1 | tail -n5
185.36.81.164
175.139.231.129
185.211.245.170
185.211.245.170
185.36.81.173
```

> Get the uniqe IP addresses:

```
$ cat /var/log/maillog | grep 'lost connection after AUTH from unknown' | cut -d'[' -f3 | cut -d ']' -f1 | sort | uniq
103.194.70.16
112.196.77.202
113.172.210.19
113.173.182.119
139.59.224.234
```

> Redirect the output to iptables:

```
$ for ip in $(cat /var/log/maillog | grep 'lost connection after AUTH from unknown' | cut -d'[' -f3 | cut -d ']' -f1 | sort | uniq); do iptables -I INPUT -s ${ip} -p tcp --dport 25 -j DROP; done
```

**[🔼Back to Top](#table-of-contents)**

## If Statements

### `Check if args are passed`

```
if [[ $# -eq 0 ]] ; then
    echo 'need to pass args'
    exit 0
fi
```

**[🔼Back to Top](#table-of-contents)**

### `Check if required variables exist`

```
if [ $1 == "one" ] || [ $1 == "two" ]
then
  echo "argument 1 has the value one or two"
  exit 0
else
  echo "I require argument 1 to be one or two"
  exit 1
fi
```

`OR`

```
NAME=${1}
if [ -z ${NAME} ]
  then
    echo NAME is undefined
    exit 1
  else
    echo "Hi ${NAME}"
fi
```

**[🔼Back to Top](#table-of-contents)**

### `Check if environment variables exists`

```
if [ -z ${OWNER} ] || [ -z ${NAME} ]
then
  echo "does not meet requirements of both environment variables"
  exit 1
else
  echo "required environment variables exists"
fi
```

**[🔼Back to Top](#table-of-contents)**

## While Loops

### `Run process for 5 Seconds`

```
set -ex
count=0
echo "boot"
ping localhost &
while [ $count -le 5 ]
  do
    sleep 1
    count=$((count + 1))
    echo $count
  done
ps aux | grep ping
echo "tear down"
kill $!
sleep 2
```

**[🔼Back to Top](#table-of-contents)**

### `Run until state changes within ttl`

```
UPDATE_COMPLETE=false
UPDATE_STATUS=running
COUNT=0
while [ ${UPDATE_COMPLETE} == false ]
    do
        if [ $count -gt 10 ]
            then
                echo "timed out"
                exit 1
        fi
        if [ ${UPDATE_STATUS} == running ] 
            then
                echo "still running"
                sleep 1
                COUNT=$((COUNT+1))
                if [ $count == 7 ]
                    then
                        UPDATE_COMPLETE=true
                fi
        elif [ ${UPDATE_STATUS} == successful ]
            then
                UPDATE_COMPLETE=successful
        else
            echo "unexpected update response"
            exit 1
        fi
    done
echo "complete"
```

**[🔼Back to Top](#table-of-contents)**

## for Loops

### `Upload all docker image`

```bash
for i in $(ls | grep .tar): do
  docker load -i $i;
done
```

**[🔼Back to Top](#table-of-contents)**

## Functions

```
message(){
    NAME=${1}
    echo "Hi ${NAME}"
}
```

`OR` ___pass all args:___

```
message(){
    echo "Hi $@"
}
```

**[🔼Back to Top](#table-of-contents)**

## Redirecting Outputs

### `Stdout, Stderr`

> Redirect stderr to /dev/null:

```
grep -irl faker . 2>/dev/null
```

> Redirect stdout to one file and stderr to another file:

```
grep -irl faker . > out 2>error
```

> Redirect stderr to stdout (&1), and then redirect stdout to a file:

```
grep -irl faker . >out 2>&1
```

> Redirect both to a file:

```
grep -irl faker . &> file.log
```

**[🔼Back to Top](#table-of-contents)**

## Manipulating Text

### `Remove first 3 characters`

```
$ STRING="abcdefghij"
$ echo ${STRING:3}
defghij
```

**[🔼Back to Top](#table-of-contents)**

### `Only show last 3 characters`

> With tail to only show the last 3 characters:

```
$ STRING="abcdefghij"
$ echo ${STRING} | tail -c 4
hij
```

**[🔼Back to Top](#table-of-contents)**
