---
title: Angular CheatSheet
description: Angular CheatSheet contains basics of angular binding & angular CLI.
created: 2022-10-24
---

## Table of Contents

- [Angular CheatSheet for Developers](#angular-cheatsheet-for-developers)
	- [What is Angular?](#what-is-angular)
	- [Angular Binding:](#angular-binding)
	- [Angular Lifecycle Hooks:](#angular-lifecycle-hooks)
	- [Angular CLI commands:](#angular-cli-commands)

# Angular CheatSheet for Developers

## What is Angular?

> Angular is an application-design framework and development platform for creating efficient and sophisticated single-page apps.

**[🔼Back to Top](#table-of-contents)**

## Angular Binding:

| Description | Command |
| ------- | ----------- |
| `One Way Binding` | `<p>title</p>` <br /> - No changes were reflected back to the variable. |
| `Two Way Binding` | `<input [(ngMo­del­)]=­"­student.F­ir­stN­ame­">` <br /> - Changes were reflected back to the variable |
| `Property Binding` | `<img [src]=­"­student.profilePicUrl">` |
| `Attribute Binding` | `<button [attr.a­ri­a-l­abe­l]=­"­ok">­Ok<­/bu­tto­n>` |
| `Class Binding` | `<div [class.Focused]="isFocused">S­ele­cte­d</­div>` |
| `ngClass` | `<div [ngClass]="assignClasses()"> <h1>{{student.FirstName}}</h1> </div>` |
| `Style Binding` | `<p [style.co­lor­]="i­sSe­lected ? 'green' : 'red'">Option {{i}}</p>` |
| `ngStyle` | `<div [ngStyle]="setStyles()"> {{student.name}} </div>` |
| `Component Binding` | `<student-details [student]="currStudent"></student-details>` |
| `Directive Binding` | `<div [ngClass] = "­{se­lected: isSele­cte­d}">­Student<­/di­v>` |
| `Event Binding` | `<button (click­)="test()">­Test</­but­ton>` |
| `$event` | `<input [value]="student.name" (input)="student.name=$event.target.value">` |

**[🔼Back to Top](#table-of-contents)**

## Angular Lifecycle Hooks:

| Command | Description |
| ------- | ----------- |
| `ngOnInit()` | It get invoked when angular initialize component or directive. |
| `ngOnChanges()` | It get invoked when angular sets data bound input property i.e. @Input(). |
| `ngDoCheck()` | It get invoked for every changes. |
| `ngAfterContentInit()` | It get invoked after angular project content in its view. |
| `ngAfterContentChecked()` | It get invoked after angular checks the binding of content into view. |
| `ngAfterViewInit()` | It get invoked after angular create component view. |
| `ngAfterViewChecked()` | It get invoked after angular checks the binding of component view. |
| `ngOnDestroy()` | It get invoked before angular destroy component or directives. |

**[🔼Back to Top](#table-of-contents)**

## Angular CLI commands:

| Command | Description |
| ------- | ----------- |
| `ng new project-name` | To create a ***new project*** |
| `ng g component <name>` | To generate a ***component*** |
| `ng g directive <name>` | To generate ***directive*** |
| `ng g pipe <name>` | To generate ***pipe*** |
| `ng g service <name>` | To generate ***service*** |
| `ng g class <name>` | To generate ***class*** |
| `ng g interface <name>` | To g ***interface*** |
| `ng serve` | ***Run application*** in local server |
| `ng build [--e=<name>]` | Create a build and change environment |
| `ng test` &#124; `e2e` | ***Testing*** your application |


| Command | Description |
| ------- | ----------- |
| `ng generate universal [options]` <br /> OR <br /> `ng g universal [options]` | - ***universal command*** <br /> - This command is used to pass this schematic to the `run` command to set up server-side rendering for an app |
| `--defaults=true` &#124; `false:` | - ***AND [options]*** <br /> - When true, it disables interactive input prompts for options with a default. |
| `--dryRun=true` &#124; `false:` | - ***AND [options]*** <br /> - When true, it runs through and reports activity without writing out results.|

**[🔼Back to Top](#table-of-contents)**
