# Visual Studio Code
Open source IDE supported by Microsoft very fast and with support for a lot extensions.



## Index
- [.. Software](../../README.md)
- [Download](#download)
- [Extensions](/Software/IDEs/VisualStudioCode/VisualStudioCode-extensions.md)
- [Tips](#tips)
  - [Show whitespaces](#tips-show-whitespaces)
  - [Sticky scroll](#tips-sticky-scroll)
  - [Enabling Source Link](#tips-enabling-source-link)
- [HotKeys (Shortcuts)](#hotkeys)
  - [Edit](#hotkeys-edit)
  - [List](#hotkeys-list)
- [Visual Studio Code for .NET](/Software/IDEs/VisualStudioCode/VisualStudioCode-dotnet.md)


## Download <a name="download"></a>
[Download](https://code.visualstudio.com/)



## Tips <a name="tips"></a>


### Show whitespaces <a name="tips-show-whitespaces"></a>

This tip it's very useful to when you are create yaml files or programming python to see the code indentation

1. Go Settings
2. Search the configuration: `editor.renderWhitespace`
3. Change to **All**

![Show whitespaces](/media/show-whitespaces.png "Show whitespaces")
> [Equivalence in visual studio](../VisualStudio.md#tips-show-whitespaces)


### Sticky scroll <a name="tips-sticky-scrol"></a>

We this feature, you have the context to where you are in the code because the sections stick at the top, e.g. a class definition, method definition, markdown headers, etc.

1. Go Settings
2. Search the configuration: `sticky`
3. Select the option `Edit > Sticky Scroll`

![Sticky scroll](/media/vscode-tips-sticky-scrol.png "Sticky scroll")


### Enabling Source Link <a name="tips-enabling-source-link"></a>
Visual Studio Code has debugger settings configured per project in the launch.json:
```json
"justMyCode": false,
"symbolOptions": {
    "searchMicrosoftSymbolServer": true,
    "searchNuGetOrgSymbolServer": true
},
"suppressJITOptimizations": true,
"env": {
    "COMPlus_ZapDisable": "1",
    "COMPlus_ReadyToRun": "0"
}
```
> [Equivalence in visual studio](../VisualStudio.md#tips-enabling-source-link)

>> Original source of the tutorial [.NET Blog](https://devblogs.microsoft.com/dotnet/improving-debug-time-productivity-with-source-link/)



## Hotkeys (Shortcuts) <a name="hotkeys"></a>

### Edit <a name="hotkeys-edit"></a>
`Menu` > `File` > `Preferences` > `Keyboard Shortcuts`


### List <a name="hotkeys-list"></a>

**Comments**
- `Ctrl` + `K` `Ctrl` + `C` : Add line comment (editor.action.addCommentLine)
- `Ctrl` + `K` `Ctrl` + `U` : Remove line comment (editor.action.removeCommentLine)

**Capitalization**
- `Ctrl` + `Shift` + `U` : Transform to uppercase (editor.action.transformToUppercase) _Modified by me_
- `Ctrl` + `U` : Transform to lowercase (editor.action.transformToLowercase) _Modified by me_

**Files**
- `Ctrl` + `Shift` + `S` : Save All (saveAll) _Modified by me_

**Duplicate line**
- `Ctrl` + `D` : Copy line current line to down (editor.action.copyLinesDownAction) _Modified by me_

**Selection**
- `Alt` + `Click with mouse` : Multiple cursors to write in multiple lines in the same time. Press `esc` to exit. [Same with vim](./VisualStudioCode-extensions.md#extensions-vim-write-multiple-lines)
- `Shift` + `Alt` + `Up Arrow` : Cursor column select up (cursorColumnSelectUp) _Modified by me_
- `Shift` + `Alt` + `Down Arrow` : Cursor column select down (cursorColumnSelectDown) _Modified by me_
- `Shift` + `Alt` + `Right Arrow` : Cursor column select right (cursorColumnSelectRight) _Modified by me_
- `Shift` + `Alt` + `Left Arrow` : Cursor column select left (cursorColumnSelectLeft) _Modified by me_