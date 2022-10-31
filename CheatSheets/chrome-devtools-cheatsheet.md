---
title: Chrome DevTools CheatSheet
description: The most commonly used keyboard shortcuts are given here.
created: 2022-10-20
---

## Table of Contents

- [Chrome DevTools Keyboard Shortcuts for Developers](#chrome-devtools-keyboard-shortcuts-for-developers)
  - [Keyboard shortcuts for opening DevTools](#keyboard-shortcuts-for-opening-devtools)
  - [Global keyboard shortcuts](#global-keyboard-shortcuts)
  - [Elements panel keyboard shortcuts](#elements-panel-keyboard-shortcuts)
  - [Styles pane keyboard shortcuts](#styles-pane-keyboard-shortcuts)
  - [Sources panel keyboard shortcuts](#sources-panel-keyboard-shortcuts)
  - [Code Editor keyboard shortcuts](#code-editor-keyboard-shortcuts)
  - [Network panel keyboard shortcuts](#network-panel-keyboard-shortcuts)
  - [Performance panel keyboard shortcuts](#performance-panel-keyboard-shortcuts)
  - [Memory panel keyboard shortcuts](#memory-panel-keyboard-shortcuts)
  - [Console panel keyboard shortcuts](#console-panel-keyboard-shortcuts)
  - [Search tab keyboard shortcuts](#search-tab-keyboard-shortcuts)

# Chrome DevTools Keyboard Shortcuts for Developers

## Keyboard shortcuts for opening DevTools

| Windows / Linux | Mac | Description |   
| :-------------: | :-: | :---------: |
| `Ctrl + Shift+ J` | `Cmd(⌘) + Option(⌥) + J`  | Open the ___Console___ panel |  
| `Ctrl + Shift + C` | `Cmd(⌘) + Shift + C` or<br />`Cmd(⌘) + Option(⌥) + C` | Open the ___Elements___ panel |
| `F12` or<br /> `Ctrl + Shift + I` | `Cmd(⌘) + Option(⌥) + I` |  Open whatever panel you used last |

**[🔼Back to Top](#table-of-contents)**

## Global keyboard shortcuts

| Windows / Linux | Mac | Description |   
| :-------------: | :-: | :---------: |
| `Ctrl + ]` | `Cmd(⌘) + ]` | Focus the next panel |
| `Ctrl + [` | `Cmd(⌘) + [` | Focus the previous panel |
| `Ctrl + Shift + M` | `Cmd(⌘) + Shift + M` | Toggle Device Mode |
| `F5` or<br /> `Ctrl + R` | `Cmd(⌘) + R` | Normal Reload | 
| `Ctrl + F5` or<br /> `Ctrl + Shift + R` | `Cmd(⌘) + Shift + R` | Hard Reload | 
| `Ctrl + Shift + +` | `Cmd(⌘) + Shift + +` | Zoom in |  
| `Ctrl + -` | `Cmd(⌘) + -` |Zoom out |  
| `Ctrl + 0` | `Cmd(⌘) + 0` | Restore default zoom level |
| `Ctrl +Shift + P` | `Cmd(⌘) + Shift + P` | Open the Command Menu |
| `Ctrl + F` | `Cmd(⌘) + F` |Search for text within the current panel. Supported only in the ___Elements___, ___Console___, ___Sources___, ___Performance___, ___Memory___, ___JavaScript Profiler___, and ___Quick Source___ panels. |

**[🔼Back to Top](#table-of-contents)**

## Elements panel keyboard shortcuts

| Windows / Linux | Mac | Description |   
| :-------------: | :-: | :---------: |
| `Ctrl + Z` | `Cmd(⌘) + Z` | Undo change | 
| `Ctrl + Y` | `Cmd(⌘) + Shift + Z` | Redo change |
| `Right Arrow(→)` | `Right Arrow(→)` |Expand the currently-selected node. <br />If the node is already expanded, this shortcut selects the element below it |  
| `Left arrow(←)` | `Left arrow(←)` | Collapse the currently-selected node. <br />If the node is already collapsed, this shortcut selects the element above it |  
| `Enter(↵)` | `Enter(↵)` | Toggle **Edit Attributes** mode on the currently-selected element | 
| `H` | `H` | Hide the currently-selected element |
| `Function + F2` | `F2` | Toggle **Edit as HTML** mode on the currently-selected element | 

**[🔼Back to Top](#table-of-contents)**

## Styles pane keyboard shortcuts

| Windows / Linux | Mac | Description |   
| :-------------: | :-: | :---------: |
| Hold `Ctrl` then click the property value | Hold `Cmd(⌘)` then click the property value | Go to the line where a property value is declared |
| Hold `Chift` then click the <br />**Color Preview** box next to the value | Hold `Shift` then click the <br />**Color Preview** box next to the value | Cycle through the RBGA, HSLA, and Hex representations of a color value |
| Click a property name or value then press `Tab(↹)` or `Shift + Tab(↹)` | Click a property name or value then press `Tab(↹)`or `Shift + Tab(↹)` | Select the next / previous property or value |
| Click a value then press the `Up Arrow(↑)` or `Down Arrow(↓)` | Click a value then press the `Up Arrow(↑)` or `Down Arrow(↓)` | Increment / decrement a property value by 1 |
| Click a value then press the `Shift + Up Arrow(↑)` or `Shift + Down Arrow(↓)` | Click a value then press the `Shift + Up Arrow(↑)` or `Shift+ Down Arrow(↓)` | Increment / decrement a property value by 10 | 
| Click a value then press the `Ctrl + Up Arrow(↑)` or `Ctrl + Down Arrow(↓)` | Click a value then press the `Cmd(⌘) + Up Arrow(↑)` or `Cmd(⌘) + Down Arrow(↓)` | Increment / decrement a property value by 100 |

**[🔼Back to Top](#table-of-contents)**

## Sources panel keyboard shortcuts

| Windows / Linux | Mac | Description |   
| :-------------: | :-: | :---------: |
| `F8` or<br />`Ctrl + \` | `F8` or<br />`Cmd(⌘) + \` | Pause script execution (if currently running) or<br />resume (if currently paused) | 
| `F10` or<br />`Ctrl + '` | `F10` or<br />`Cmd(⌘) + '` | Step over next function call | 
| `F11` or<br />`Ctrl + ;` | `F11` or<br />`Cmd(⌘) + ;` | Step into next function call | 
| `Shift + F11` or<br />`Ctrl + Shift + ;` | `Shift + F11` or<br />`Cmd(⌘) + Shift + ;` | Step out of current function | 
| `Ctrl + S` | `Cmd(⌘) + S`  | Save changes to local modifications |
| `Ctrl + Alt + S` | `Cmd(⌘) + Option(⌥) + S`  | Save all changes |
| `Ctrl + G`  | `Ctrl + G` | Go to line |
| `Alt + W` | `Option(⌥) + W`  | Close the active tab |  
| `Ctrl + Shift + Y` | `Cmd(⌘) + Shift + Y` | Toggle the **Navigation** sidebar on the left |
| `Ctrl + Shift + H` |  `Cmd(⌘)+ Shift + H`  |Toggle the **Debugger** sidebar on the right |

**[🔼Back to Top](#table-of-contents)**

## Code Editor keyboard shortcuts

| Windows / Linux | Mac | Description |   
| :-------------: | :-: | :---------: |
| `Ctrl + Delete(del)` | `Option(⌥) + Delete(del)` | Delete all characters in the last word, up to the cursor | 
| `Ctrl + M` | `Ctrl + M` | Go to matching bracket |
| `Ctrl + B` | `Cmd + B` | Add or remove a line-of-code breakpoint |
| `Ctrl + D` or <br /> `Ctrl + U` | `Cmd + D` or <br /> `Cmd + U` | Select / de-select the next occurrence of whatever word the cursor is on. Each occurrence is highlighted simultaneously |
| `Ctrl + /` | `Cmd(⌘) + /` | Toggle single-line comment. <br /> If multiple lines are selected, DevTools adds a comment to the start of each line |

**[🔼Back to Top](#table-of-contents)**

## Network panel keyboard shortcuts

| Windows / Linux | Mac | Description |   
| :-------------: | :-: | :---------: |
| `Ctrl + E` | `Cmd(⌘) + E` | Start/stop recording | 
| `Ctrl + R` | `Cmd(⌘) + R` | Record a reload | 
| `R` | `R` | Replay a selected XHR request |
| `Escape(esc)` | `Escape(esc)` | Hide the details of a selected request |

**[🔼Back to Top](#table-of-contents)**

## Performance panel keyboard shortcuts

| Windows / Linux | Mac | Description |   
| :-------------: | :-: | :---------: |
| `Ctrl + E` | `Cmd(⌘) + E` | Start/stop recording |
| `Ctrl + S` | `Cmd(⌘) + S` | Save recording |
| `Ctrl + O` | `Cmd(⌘) + O` | Load recording | 

**[🔼Back to Top](#table-of-contents)**

## Memory panel keyboard shortcuts

| Windows / Linux | Mac | Description |   
| :-------------: | :-: | :---------: |
| `Ctrl + E` | `Cmd(⌘)+ E` | Start/stop recording |

**[🔼Back to Top](#table-of-contents)**

## Console panel keyboard shortcuts

| Windows / Linux | Mac | Description |   
| :-------------: | :-: | :---------: |
| `Right Arrow(→)` or<br />`Tab(↹)` | `Right Arrow(→)` or<br />`Tab(↹)` |Accept autocomplete suggestion | 
| `Escape(esc)` | `Escape(esc)` | Reject autocomplete suggestion |
| `Up Arrow(↑)` | `Up Arrow(↑)` | Get previous statement |
| `Down Arrow(↓)` | `Down Arrow(↓)` | Get next statement |
| `Ctrl + `\` | `Ctrl + `\` | Focus the **Console** |
| `Ctrl + L` | `Cmd(⌘) + K` or<br />`Option(⌥) + L` | Clear the **Console** |

**[🔼Back to Top](#table-of-contents)**

## Search tab keyboard shortcuts

| Windows / Linux | Mac | Description |   
| :-------------: | :-: | :---------: |
| `Ctrl + Shift + {` or<br />`Ctrl + Shift + }` | `Cmd(⌘) + Option(⌥) + {` or<br />`Cmd(⌘) + Option(⌥) + }` | Expand/collapse all search results |

**[🔼Back to Top](#table-of-contents)**