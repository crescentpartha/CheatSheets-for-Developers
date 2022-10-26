---
title: NVM CheatSheet
description: The most commonly used nvm commands are given here.
created: 2022-10-19
---

## Table of Contents

- [NVM CheatSheet for Developers](#nvm-cheatsheet-for-developers)
  - [Basic Syntax of Node Version Manager](#basic-syntax-of-node-version-manager)

# NVM CheatSheet for Developers

## Basic Syntax of Node Version Manager

| Command                         | Description                         |
| ------------------------------- | ----------------------------------- |
| `nvm ls-remote`                 | Lists all available versions of Node|
| `nvm ls`                        | Lists all locally installed versions|
| `nvm install node`              | Installs the newest release of Node |
| `nvm install <version>`         | Installs the given release of Node  |
| `nvm use <version>`             | Switches and uses the given Node release|
| `nvm which <version>`           | Shows path to the given Node version|
| `nvm current`                   | Shows what is the currently used Node version|
| `nvm alias default <version>`   | Sets the default Node version to the given version|
| `nvm unalias <alias_name>`      | Deletes the alias named <alias_name> |
| `nvm --help`                    | Shows NVM help documents.           |
| `nvm exec <version> node app.js`| Run Node app.js with the PATH pointing to given node version|
| `nvm set-colors cgYmW`          | Set text colors to cyan, green, bold yellow, magenta, and white|
| `nvm run <version> app.js`      | Run app.js using given Node version |
| `nvm install-latest-npm`        | Update your version of npm if you use Node installed through nvm |
| `nvm root <path>`               | Set the directory where nvm should store different versions of node.js.|
| `nvm proxy [url]`               | Set a proxy to use for downloads. Leave [url] blank to see the current proxy. Set [url] to "none" to remove the proxy.|
| `nvm -v`                        | Check if nvm is installed                                                                                              |
| `nvm uninstall <version>`       | Un-Install a specific version                                                                                          |
| `nvm ls`                        | Show versions available locally                                                                                        |
| `nvm uninstall --lts`           | Uninstall the latest long term support version |

**[🔼Back to Top](#table-of-contents)**
