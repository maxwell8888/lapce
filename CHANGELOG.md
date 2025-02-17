# Changelog

## Unreleased

### Features/Changes

### Bug Fixes

## 0.2.1

### Features/Changes
- [#1050](https://github.com/lapce/lapce/pull/1050): Collapse groups of problems in the problem list panel
- [#1165](https://github.com/lapce/lapce/pull/1165): Command to reveal item in system file explorer
- [#1196](https://github.com/lapce/lapce/pull/1196): Always show close button on focused editor tabs
- [#1208](https://github.com/lapce/lapce/pull/1208): Sticky header breadcrumbs
  - This provides a header at the top which tells you information about the current scope! Especially useful for long blocks of code
  - ![image](https://user-images.githubusercontent.com/13157904/195404556-2c329ebb-f721-4d55-aa22-56a54f8e8454.png)
  - As well, you can see that there is now a breadcrumb path to the current file. 
  - A language with syntax highlighting can have this added, even without an LSP. Take a look at `language.rs` if your language isn't supported!
- [#1198](https://github.com/lapce/lapce/pull/1198): Focus current theme/language in palette
- [#1244](https://github.com/lapce/lapce/pull/1244); Prettier plugin panel
- [#1238](https://github.com/lapce/lapce/pull/1238): Improved multicursor selection
- [#1291](https://github.com/lapce/lapce/pull/1291): Use link colour for empty editor buttons
- [#1234](https://github.com/lapce/lapce/commit/07390f0c90c0700d1f69409bf48723d15090c474): Automatic line height
- [#1262](https://github.com/lapce/lapce/pull/1262): Add absolute/relative copy path to file explorer
- [#1284](https://github.com/lapce/lapce/pull/1284): Render whitespace (default: none)
  - ![image](https://user-images.githubusercontent.com/13157904/195410868-f27db85f-d7d2-4197-84f0-12d6c44e2053.png)
- [#1308](https://github.com/lapce/lapce/pull/1308): Handle LSP ResourceOp
- [#1251](https://github.com/lapce/lapce/pull/1251): Add vim's paste-before `P` command
- [#1319](https://github.com/lapce/lapce/pull/1319): Add information page for plugins
- [#1344](https://github.com/lapce/lapce/pull/1344): Replace the branch-selector menu with a scrollable list
- [#1352](https://github.com/lapce/lapce/pull/1352): Add duplicate line up/down commands
- [#1281](https://github.com/lapce/lapce/pull/1281): Implement logic for displaying plugin installation status
- [#1353](https://github.com/lapce/lapce/pull/1353): Implement syntax aware selection
- [#1358](https://github.com/lapce/lapce/pull/1358): Add autosave implementation
- [#1381](https://github.com/lapce/lapce/pull/1381): Show multiple hover items in the hover box
- [#1040](https://github.com/lapce/lapce/pull/1040): Add keybindings for `Shift-Del`, `Shift-Ins`, and `Ctrl-Ins`
- [#1401](https://github.com/lapce/lapce/pull/1401): Merge semantic and tree-sitter syntax highlighting
- [1426](https://github.com/lapce/lapce/pull/1426): Add cursor position/current selection in status bar
  - ![image](https://user-images.githubusercontent.com/13157904/195414557-dbf6cff1-3ab2-49ec-ba9d-c7507b2fc83a.png)
- [#1420](https://github.com/lapce/lapce/pull/1420): Add LSP `codeAction/resolve` support
- [#1440](https://github.com/lapce/lapce/pull/1440): IME support
- [#1449](https://github.com/lapce/lapce/pull/1449): Plugin settings in the editor support. Though this still needs some work from plugins to expose them all nicely!
- [#1441](https://github.com/lapce/lapce/pull/1441): Button for Case-Sensitive search
- [#1471](https://github.com/lapce/lapce/pull/1471): Add command to (un)install Lapce from/to PATH
- [#1419](https://github.com/lapce/lapce/pull/1419): Add atomic soft tabs: now you can move your cursor over four spaces as if it was a single block

### Syntax / Extensions
- [#957](https://github.com/lapce/lapce/pull/957): Replace existing tree-sitter syntax highlighting code with part of Helix's better implementation
  - This means that syntax highlighting for more languages! Such as fixing markdown support, and making so that languages embedded in others (like JavaScript in HTML) work.
  - Note that not all themes have updated themselves to include the extra scopes/colors.
- [#1036](https://github.com/lapce/lapce/pull/1036): Recognize ESM/CJS extensions for JavaScript/TypeScript
- [#1007](https://github.com/lapce/lapce/pull/1007): Add ability to bind a key shortcut for quitting the editor
- [#1104](https://github.com/lapce/lapce/pull/1104): Add syntax highlighting for Dockerfile, C#, and Nix
- [#1118](https://github.com/lapce/lapce/pull/1118): Recognize `pyi, pyc, pyd, pyw` extensions for Python
- [#1122](https://github.com/lapce/lapce/pull/1122): Recognize extensions for DLang
  - [#1335](https://github.com/lapce/lapce/pull/1335): Highlighting for DLang
- [#1153](https://github.com/lapce/lapce/pull/1050): Recognize and add highlighting for Dart
- [#1161](https://github.com/lapce/lapce/pull/1161): Recognize and add highlighting for Svelte and LaTeX files
- [#1299](https://github.com/lapce/lapce/pull/1299): Recognize and add highlighting for Kotlin
- [#1326](https://github.com/lapce/lapce/pull/1326): Recognize and add highlighting for Vue
- [#1370](https://github.com/lapce/lapce/pull/1370): Recognize and add highlighting for R
- [#1416](https://github.com/lapce/lapce/pull/1416): Recognize and add highlighting for Scheme
- [#1145](https://github.com/lapce/lapce/pull/1145): Adds/Fixes highlighting for C/C++/TypeScript/JavaScript/Zig/Bash
- [#1272](https://github.com/lapce/lapce/pull/1272): Adds/Fixes highlighting for Elm/JSX/TSX
- [#1450](https://github.com/lapce/lapce/pull/1450): Add `tf` extension for HCL

### Bug Fixes
- [#1030](https://github.com/lapce/lapce/pull/1030): Don't try to open an font file with an empty name if there is no font family set
- [9f0120d](https://github.com/lapce/lapce/commit/9f0120df85e3aaaef7fbb43385bb15d88443260a): Fix excessive CPU usage in part of the code
- [bf5a98a](https://github.com/lapce/lapce/commit/bf5a98a6d432f9d2abdc1737da2d075e204771fb): Fix issue where sometimes Lapce can't open
- [#1084](https://github.com/lapce/lapce/pull/1084): Use host shell in terminal when running inside Flatpak
- [#1120](https://github.com/lapce/lapce/pull/1120): Make Alt+Backspace work in the terminal properly
- [#1127](https://github.com/lapce/lapce/pull/1127): Improve Julia highlighting
- [#1179](https://github.com/lapce/lapce/pull/1179): Various improvements/fixes to window-tab functionality
- [#1210](https://github.com/lapce/lapce/pull/1210): Fixed closing modified file when closing split
- [#1219](https://github.com/lapce/lapce/pull/1219): Fix append command behavior
- [#1250](https://github.com/lapce/lapce/pull/1250): Fix too long socket path for proxy
- [#1252](https://github.com/lapce/lapce/pull/1252): Check whether the active editor tab index actually exists, avoiding a potential crash
- [#1294](https://github.com/lapce/lapce/pull/1294): Backward word deletion should respect whitespace better
- [#1301](https://github.com/lapce/lapce/pull/1301): Fix incorrect path when going from Url -> PathBuf (such as from an LSP)
- [#1368](https://github.com/lapce/lapce/pull/1368): Fix tabstop for postfix completions
- [#1388](https://github.com/lapce/lapce/pull/1388): Fix regex search within the terminal
- [#1423](https://github.com/lapce/lapce/pull/1423): Fix multiple cursor offset after inserting opening pair
- [#1434](https://github.com/lapce/lapce/pull/1434): Join PATH with correct platform separator
- [#1443](https://github.com/lapce/lapce/pull/1443): Correct terminal font sizing
- [#1453](https://github.com/lapce/lapce/pull/1453): Trim whitespace from search results
- [#1461](https://github.com/lapce/lapce/pull/1461): Load shell environment when launching from GUI
- Many more fixes!

### Other
- [#1191](https://github.com/lapce/lapce/pull/1191): Tone down default inlay hint background color in Lapce dark theme
- [#1227](https://github.com/lapce/lapce/pull/1227): Don't restore cursor mode on undo
- [#1413](https://github.com/lapce/lapce/pull/1413): Disable format-on-save by default. Remember to re-enable this if you want it!
- [#1404](https://github.com/lapce/lapce/pull/1404): Log panics with full backtrace as errors
