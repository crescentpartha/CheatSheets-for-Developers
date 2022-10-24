---
title: NPM CheatSheet
description: The most commonly used npm commands are given here.
created: 2022-10-18
---

## Table of Contents

- [NPM CheatSheet for Developers](#npm-cheatsheet-for-developers)
  - [Basic Syntax of Node Package Manager](#basic-syntax-of-node-package-manager)

# NPM CheatSheet for Developers

## Basic Syntax of Node Package Manager

| Command                                                        | Description                                          |
| -------------------------------------------------------------- | ---------------------------------------------------- |
| `npm init`                                                     | Initialize a node.js project                         |
| `npm install` <br /> `npm i`                                   | Install package.json dependencies                    |
| `npm install --global [package]` <br /> `npm i -g [package]`   | install package globally                             |
| `npm install-latest-npm`                                       | Update npm                                           |
| `npm run`                                                      | List available scripts to run                        |
| `npm run bar`                                                  | Runs the script named bar                            |
| `npm test`                                                     | Runs the projects tests                              |
| `npm list`                                                     | For Local packages                                   |
| `npm un <package_name> ` <br /> `npm uninstall <package_name>` | Uninstall package from project                       |
| `npm -g uninstall <name> `                                     | Uninstall global package                             |
| `npm update -g <package_name> `                                | Update individual global package(s)                  |
| `npm up <package_name>`                                        | Update npm package                                   |
| `npm list -g --depth-0`                                        | List globally installed packages                     |
| `npm-windows-upgrades`                                         | Upgrade npm on Windows                               |
| `npm outdated -g --depth-0`                                    | Updated global packages                              |
| `npm alias default 16`                                         | Make a node version default                          |
| `npm i <package>`                                              | Install a package                                    |
| `npm u <package>`                                              | Update the package                                   |
| `npm rm <package>`                                             | Remove a package                                     |
| `npm audit`                                                    | Scan and list all the vulnerabilities in the package |
| `npm audit fix`                                                | Fix found vulnerabilities                            |
| `npm edit`                                                     | Edit an installed package                            |
| `npm publish`                                                  | Publish a package                                    |
| `npm rebuild`                                                  | - Rebuild a package <br /> - This command runs the `npm build` command on the matched folders |

**[🔼Back to Top](#table-of-contents)**
