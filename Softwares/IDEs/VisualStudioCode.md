# Visual Studio Code
Open source IDE supported by Microsoft very fast and with support for a lot extensions.



## Index
- [.. Softwares](/Softwares/README.md)
- [Download](#download)
- [Extensions](#extensions)
  - [GitHub Actions](#extensions-github-actions)
  - [Docker](#extensions-github-docker)
  - [Task list](#extensions-tasklist)
  - [Back & Forth](#extensions-back-forth)
  - [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
  - [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
  - [Highlight Trailing White Spaces](https://marketplace.visualstudio.com/items?itemName=ybaumes.highlight-trailing-white-spaces)
  - [JWT Decoder](https://marketplace.visualstudio.com/items?itemName=jflbr.jwt-decoder)
  - [Vim](#extensions-vim)
- [Tips](#tips)
  - [Show whitespaces](#tips-show-whitespaces)
  - [Enabling Source Link](#tips-enabling-source-link)
- [HotKeys (Shortcuts)](#hotkeys)
  - [Edit](#hotkeys-edit)
  - [List](#hotkeys-list)
- [Visual Studio Code for .NET](/Softwares/IDEs/VisualStudioCode-dotnet.md)


## Download <a name="download"></a>
[Download](https://code.visualstudio.com/)



## Extensions <a name="extensions"></a>


### GitHub Actions <a name="extensions-github-actions"></a>
Extension with IntelliSense code and very good to management GitHub Actions.

[Download](https://marketplace.visualstudio.com/items?itemName=cschleiden.vscode-github-actions)


### Docker <a name="extensions-github-docker"></a>
The Docker extension makes it easy to build, manage, and deploy containerized applications from Visual Studio Code. It also provides one-click debugging of Node.js, Python, and .NET Core inside a container.
You can get IntelliSense when editing your Dockerfile and docker-compose.yml files, with completions and syntax help for common commands.

[Download](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)


### Task List <a name="extensions-tasklist"></a>
A extensions to show all your tags TODOs, FIXMEs, etc.
- [Todo Tree](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree)
- [TODO Highlight](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight)
> [Equivalence in visual studio](./VisualStudio.md#tools-tasklist)


### Back & Forth <a name="extensions-back-forth"></a>
Extension for VSCode adds go back/forward buttons to the title bar for easier navigation through recent edit locations and opened files.

[Download](https://marketplace.visualstudio.com/items?itemName=nick-rudenko.back-n-forth)


### Vim <a name="extensions-vim"></a>
[Download](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)

#### Write in multiple lines <a name="extensions-vim-write-multiple-lines"></a>

1. `Ctrl` + `V`
2. `J` (Multiple times): To select the line
3. `Shift` + `I`: Start in edit mode
4. `Esc`: To finish



### Tips <a name="tips"></a>


#### Show whitespaces <a name="tips-show-whitespaces"></a>

This tip it's very useful to when you are create yaml files or programming python to see the code indentation

1. Go Settings
2. Search the configuration: `editor.renderWhitespace`
3. Change to **All**

![Show whitespaces](/media/show-whitespaces.png "Show whitespaces")
> [Equivalence in visual studio](./VisualStudio.md#tips-show-whitespaces)


#### Enabling Source Link <a name="tips-enabling-source-link"></a>
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

>> Original source of the tutorial [.NET Blog](https://devblogs.microsoft.com/dotnet/improving-debug-time-productivity-with-source-link/)



### Hotkeys (Shortcuts)<a name="hotkeys"></a>

#### Edit <a name="hotkeys-edit"></a>
`Menu` > `File` > `Preferences` > `Keyboard Shortcuts`


#### List <a name="hotkeys-list"></a>

**To write**
- `Alt` + `Click with mouse` : Multiple cursors to write in multiple lines in the same time. Press `esc` to exit. [With vim](#extensions-vim-write-multiple-lines)

**Comments**
- `Ctrl` + `K` `Ctrl` + `C` : Add line comment (editor.action.addCommentLine)
- `Ctrl` + `K` `Ctrl` + `U` : Remove line comment (editor.action.removeCommentLine)

**Capitalization**
- `Ctrl` + `Shift` + `U` : Transform to uppercase (editor.action.transformToUppercase) _Modified by me_
- `Ctrl` + `U` : Transform to lowercase (editor.action.transformToLowercase) _Modified by me_

**Files**
- `Ctrl` + `Shift` + `S` : Save All (saveAll) _Modified by me_