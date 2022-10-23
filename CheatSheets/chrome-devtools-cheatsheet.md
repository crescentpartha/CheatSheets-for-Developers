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

| Action | Mac  | Windows/Linux  | 
| :----: | :--: | :------------: |
| Open the ___Console___ panel | `cmd(⌘)+option(⌥)+j` | `ctrl+shift+j` | 
| Open the ___Elements___ panel | `cmd(⌘)+shift+c` or<br />`cmd(⌘)+option(⌥)+c`   | `ctrl+shift+c` | 
| Open whatever panel you used last | `cmd(⌘)+option(⌥)+i` | `F12` or<br /> `ctrl+shift+i` |

**[🔼Back to Top](#table-of-contents)**

## Global keyboard shortcuts

| Action                     | Mac           | Windows/Linux        | 
| :----:                     | :---:         | :-----------:        |
| Focus the next panel       | `cmd(⌘)+]`       | `ctrl+]`     |
| Focus the previous panel   | `cmd(⌘)+[`       | `ctrl+[`     |
| Toggle Device Mode         | `cmd(⌘)+shift+m` | `ctrl+shift+m` |
| Normal Reload              | `cmd(⌘)+r`       | `F5` or<br /> `ctrl+r` |
| Hard Reload                | `cmd(⌘)+shift+r` | `ctrl+F5` or<br /> `ctrl+shift+r` | 
| Zoom in                    | `cmd(⌘)+shift++` | `ctrl+shift++` |
| Zoom out                   | `cmd(⌘)+-`       | `ctrl+-` |
| Restore default zoom level | `cmd(⌘)+0`       | `ctrl+0` |

**[🔼Back to Top](#table-of-contents)**

## Elements panel keyboard shortcuts

| Action      | Mac           | Windows/Linux  | 
| :----:      | :---:         | :-----------:  |
| Undo change | `cmd(⌘)+z`       | `ctrl+z`       |
| Redo change | `cmd(⌘)+shift+z` | `ctrl+y` | 
| Expand the currently-selected node. <br />If the node is already expanded, this shortcut selects the element below it | `right arrow(→)` | `right arrow(→)` | 
| Collapse the currently-selected node. <br />If the node is already collapsed, this shortcut selects the element above it | `left arrow(←)` | `left arrow(←)` | 
| Toggle **Edit Attributes** mode on the currently-selected element | `enter(↵)` | `enter(↵)` | 
| Hide the currently-selected element | `h` | `h` | 
| Toggle **Edit as HTML** mode on the currently-selected element | `function+F2` | `F2` | 

**[🔼Back to Top](#table-of-contents)**

## Styles pane keyboard shortcuts

| Action      | Mac           | Windows/Linux  | 
| :----:      | :---:         | :-----------:  |
| Go to the line where a property value is declared | Hold `cmd(⌘)` then click the property value | Hold `ctrl` then click the property value |
| Cycle through the RBGA, HSLA, and Hex representations of a color value | Hold `shift` then click the <br />**Color Preview** box next to the value | Hold `shift` then click the <br />**Color Preview** box next to the value |
| Select the next / previous property or value | Click a property name or value then press `tab(↹)` or `shift+tab(↹)` | Click a property name or value then press `tab(↹)`or `shift+tab(↹)` |
| Increment / decrement a property value by 1 | Click a value then press the `up arrow(↑)` or `down arrow(↓)` | Click a value then press the `up arrow(↑)` or `down arrow(↓)` |
| Increment / decrement a property value by 10 | Click a value then press the `shift+up arrow(↑)` or `shift+down arrow(↓)` | Click a value then press the `shift+up arrow(↑)` or `shift+down arrow(↓)` |
| Increment / decrement a property value by 100 | Click a value then press the `cmd(⌘)+up arrow(↑)` or `cmd(⌘)+down arrow(↓)` | Click a value then press the `ctrl+up arrow(↑)` or `ctrl+down arrow(↓)` |

**[🔼Back to Top](#table-of-contents)**

## Sources panel keyboard shortcuts

| Action      | Mac           | Windows/Linux  | 
| :----:      | :---:         | :-----------:  |
| Pause script execution (if currently running) or<br />resume (if currently paused) | `F8` or<br />`cmd(⌘)+\` | `F8` or<br />`ctrl+\` |
| Step over next function call | `F10` or<br />`cmd(⌘)+'` | `F10` or<br />`ctrl+'` |
| Step into next function call | `F11` or<br />`cmd(⌘)+;` | `F11` or<br />`ctrl+;` |
| Step out of current function | `shift+F11` or<br />`cmd(⌘)+shift+;` | `shift+F11` or<br />`ctrl+shift+;` |
| Save changes to local modifications | `cmd(⌘)+s`  | `ctrl+s` |
| Save all changes | `cmd(⌘)+option(⌥)+s`  | `ctrl+alt+s` |
| Go to line | `ctrl+g`  | `ctrl+g` |
| Close the active tab | `option(⌥)+w`  | `alt+w` |
| Toggle the **Navigation** sidebar on the left | `cmd(⌘)+shift+y`  | `ctrl+shift+y` |
| Toggle the **Debugger** sidebar on the right | `cmd(⌘)+shift+h`  | `ctrl+shift+h` |

**[🔼Back to Top](#table-of-contents)**

## Code Editor keyboard shortcuts

| Action      | Mac           | Windows/Linux  | 
| :----:      | :---:         | :-----------:  |
| Delete all characters in the last word, up to the cursor | `option(⌥)+delete(del)` | `ctrl+delete(del)` |
| Go to matching bracket | `ctrl+m` | `ctrl+m` |
| Toggle single-line comment.<br />If multiple lines are selected, DevTools adds a comment to the start of each line | `cmd(⌘)+/` | `ctrl+/` |



**[🔼Back to Top](#table-of-contents)**

## Network panel keyboard shortcuts

| Action      | Mac           | Windows/Linux  | 
| :----:      | :---:         | :-----------:  |
| Start/stop recording | `cmd(⌘)+e` | `ctrl+e` |
| Record a reload | `cmd(⌘)+r` | `ctrl+r` |
| Replay a selected XHR request | `r` | `r` |
| Hide the details of a selected request | `escape(esc)` | `escape(esc)` |

**[🔼Back to Top](#table-of-contents)**

## Performance panel keyboard shortcuts

| Action      | Mac           | Windows/Linux  | 
| :----:      | :---:         | :-----------:  |
| Start/stop recording | `cmd(⌘)+e` | `ctrl+e` |
| Save recording | `cmd(⌘)+s` | `ctrl+s` |
| Load recording | `cmd(⌘)+o` | `ctrl+o` |

**[🔼Back to Top](#table-of-contents)**

## Memory panel keyboard shortcuts

| Action      | Mac           | Windows/Linux  | 
| :----:      | :---:         | :-----------:  |
| Start/stop recording | `cmd(⌘)+e` | `ctrl+e` |

**[🔼Back to Top](#table-of-contents)**

## Console panel keyboard shortcuts

| Action      | Mac           | Windows/Linux  | 
| :----:      | :---:         | :-----------:  |
| Accept autocomplete suggestion | `right arrow(→)` or<br />`tab(↹)` | `right arrow(→)` or<br />`tab(↹)` |
| Reject autocomplete suggestion | `escape(esc)` | `escape(esc)` |
| Get previous statement | `up arrow(↑)` | `up arrow(↑)` |
| Get next statement | `down arrow(↓)` | `down arrow(↓)` |
| Focus the **Console** | `ctrl+\` | `down arrow(↓)` |
| Clear the **Console** | `down arrow(↓)` | `down arrow(↓)` |

**[🔼Back to Top](#table-of-contents)**

## Search tab keyboard shortcuts

| Action      | Mac           | Windows/Linux  | 
| :----:      | :---:         | :-----------:  |
| Expand/collapse all search results | `cmd(⌘)+option(⌥)+{` or<br />`cmd(⌘)+option(⌥)+}` | `ctrl+shift+{` or<br />`ctrl+shift+}` |

**[🔼Back to Top](#table-of-contents)**