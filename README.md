# VS Code Config

### User Snippets
> File > Preferences > User Snippets

```javascript
{
  // Place your global snippets here. Each snippet is defined under a snippet name and has a scope, prefix, body and
  // description. Add comma separated ids of the languages where the snippet is applicable in the scope field. If scope
  // is left empty or omitted, the snippet gets applied to all languages. The prefix is what is
  // used to trigger the snippet and the body will be expanded and inserted. Possible variables are:
  // $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders.
  // Placeholders with the same ids are connected.
  // Example:
  "Import Routes": {
    "scope": "javascript,javascriptreact",
    "prefix": "imbrx",
    "body": ["import { Routes, Route } from 'react-router-dom';"],
    "description": "import routesm route from react router"
  },
  "nexp": {
    "prefix": "nexpr",
    "body": [
      "const express = require('express')",
      "const app = express()",
      "//const cors = require('cors')",
      "//require('dotenv').config()",
      "const PORT = $1",
      "",
      "//app.use(cors())",
      "",
      "app.get('/', (req, res) => {",
      "  res.send('Hello World!')",
      "})",
      "",
      "app.listen(PORT, () => {",
      "  console.log(`http://localhost:${PORT}`)",
      "})"
    ],
    "description": "Scaffold expressjs snippet"
  }
}

```

### Keybindings

`keybindings.json` is located in `~/.config/Code/User`

  ```javascript
  // VSCODE ON COKE

// Place your key bindings in this file to overwrite the defaults
// ALT + I/J/K/L: up/left/down/right
// CTRL + ALT + I/K: auto suggestion selection similar to arrow keys
// ALT + SHIFT + I/J/K/L: mark text up/left/down/right
// CTRL + J/L: send cursor to start/end of line
// CTRL + ALT + J/L: send cursor to start/end of word
// CTRL + ALT + U/O: send cursor to "wordPartLeft"/"wordPartRight"
// CTRL + ALT +  SHIFT + U/O: mark from cursor to "wordPartLeft"/"wordPartRight"
// CTRL + ALT + Y: got to declaration
// CTRL + I/K: add/remove another cursor up/down

// -- IF LINEJUMPER IS INSTALLED -- //
// CTRL + ALT + I/K: move cursor 10 lines up/down
// CTRL + ALT + SHIFT + I/K: mark 10 lines up/down

[
  {
    "key": "ctrl+alt+i",
    "command": "selectPrevSuggestion",
    "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
  },
  {
    "key": "ctrl+alt+k",
    "command": "selectNextSuggestion",
    "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
  },
  // {
  //   "key": "ctrl+shift+i",
  //   "command": "editor.action.moveLinesUpAction",
  //   "when": "editorTextFocus"
  // },
  // {
  //   "key": "ctrl+shift+k",
  //   "command": "editor.action.moveLinesDownAction",
  //   "when": "editorTextFocus"
  // },
  {
    "key": "alt+k",
    "command": "cursorDown",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+i",
    "command": "cursorUp",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+l",
    "command": "cursorRight",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+j",
    "command": "cursorLeft",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+shift+k",
    "command": "cursorDownSelect",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+shift+i",
    "command": "cursorUpSelect",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+shift+l",
    "command": "cursorRightSelect",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+shift+j",
    "command": "cursorLeftSelect",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+ctrl+l",
    "command": "cursorWordEndRight",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+ctrl+j",
    "command": "cursorWordStartLeft",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+shift+ctrl+l",
    "command": "cursorWordRightSelect",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+shift+ctrl+j",
    "command": "cursorWordLeftSelect",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+shift+o",
    "command": "cursorEndSelect",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+shift+u",
    "command": "cursorHomeSelect",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+l",
    "command": "cursorEnd",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+j",
    "command": "cursorHome",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+alt+y",
    "command": "editor.action.goToDeclaration"
  },
  {
    "key": "ctrl+i",
    "command": "cursorColumnSelectUp",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+k",
    "command": "cursorColumnSelectDown",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+shift+ctrl+o",
    "command": "cursorWordPartRightSelect",
    "when": "textInputFocus"
  },
  {
    "key": "alt+shift+ctrl+u",
    "command": "cursorWordPartLeftSelect",
    "when": "textInputFocus"
  },
  {
    "key": "alt+ctrl+o",
    "command": "cursorWordPartRight",
    "when": "textInputFocus"
  },
  {
    "key": "alt+ctrl+u",
    "command": "cursorWordPartLeft",
    "when": "textInputFocus"
  }
  //   {
  //     "key": "alt+ctrl+k",
  //     "command": "lineJumper.moveDown",
  //     "when": "editorTextFocus"
  //   },
  //   {
  //     "key": "alt+ctrl+i",
  //     "command": "lineJumper.moveUp",
  //     "when": "editorTextFocus"
  //   },
  //   {
  //     "key": "alt+shift+ctrl+k",
  //     "command": "lineJumper.selectDown",
  //     "when": "editorTextFocus"
  //   },
  //   {
  //     "key": "alt+shift+ctrl+i",
  //     "command": "lineJumper.selectUp",
  //     "when": "editorTextFocus"
  //   }
]

  ```
