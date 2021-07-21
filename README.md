# Dev tips
Tips, tools and software to improve development




## Index
- [Softwares](#softwares)
  - [IDE's](#softwares-ides)
    - [Visual Studio Code](#softwares-ides-vscode)
      - [Extensions](#softwares-ides-vscode-extensions)
        - [GitHub Actions](#softwares-ides-vscode-extensions-github-actions)
        - [Docker](#softwares-ides-vscode-extensions-github-docker)
- [Tools](#tools)
  - [Windows Terminal](#tools-windows-terminal)
    - [Git customization](#tools-windows-terminal-gitcustomization)
    - [Windows terminal customization](#tools-windows-terminal-customization)




## Softwares <a name="softwares"></a>


### IDE's <a name="softwares-ides"></a>



### Visual Studio Code <a name="softwares-ides-vscode"></a>
Open source IDE supported by Microsoft very fast and with support for a lot extensions.
[Download](https://code.visualstudio.com/)


#### Extensions <a name="softwares-ides-vscode-extensions"></a>

##### GitHub Actions <a name="softwares-ides-vscode-extensions-github-actions"></a>
Extension with IntelliSense code and very good to management GitHub Actions.
[Download](https://marketplace.visualstudio.com/items?itemName=cschleiden.vscode-github-actions)

##### Docker <a name="softwares-ides-vscode-extensions-github-docker"></a>
The Docker extension makes it easy to build, manage, and deploy containerized applications from Visual Studio Code. It also provides one-click debugging of Node.js, Python, and .NET Core inside a container.
You can get IntelliSense when editing your Dockerfile and docker-compose.yml files, with completions and syntax help for common commands.
[Download](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)




## Tools <a name="tools"></a>


### Windows Terminal <a name="tools-windows-terminal"></a>
Windows terminal is a new Microsoft open source CLI with support to multiple terminals like a command prompt, PowerShell, git CLI, Azure Cloud Shell, etc...
[Download](https://docs.microsoft.com/en-us/windows/terminal/get-started)

#### Git customization <a name="tools-windows-terminal-gitcustomization"></a>

**Install git support**
```bash
Install-Module posh-git -Scope CurrentUser -Force
```

**Install support for themes**
```bash
Install-Module oh-my-posh -Scope CurrentUser
```

**Edit profile**
```bash
code $PROFILE
```

**Load modules and theme. Add next code in end of file**
```bash
Import-Module posh-git
Import-Module oh-my-posh
Set-PoshPrompt -Theme slimfat
```

**Install font to support theme icons**

[Download](https://github.com/romkatv/dotfiles-public/blob/master/.local/share/fonts/NerdFonts/MesloLGS%20NF%20Regular.ttf)

#### Windows terminal customization <a name="tools-windows-terminal-customization"></a>

Settings > Open JSON file
```json
"profiles":
{
  "defaults":
  {
    "acrylicOpacity": 0.89,
    "colorScheme": "Dracula",
    "fontFace": "MesloLGS NF Regular",
    "fontSize": 10,
    "useAcrylic": true
  },
    
    ...

"schemes":
[
  {
    "name": "Dracula",
    "cursorColor": "#F8F8F2",
    "selectionBackground": "#44475A",
    "background": "#282A36",
    "foreground": "#F8F8F2",
    "black": "#21222C",
    "blue": "#BD93F9",
    "cyan": "#8BE9FD",
    "green": "#50FA7B",
    "purple": "#FF79C6",
    "red": "#FF5555",
    "white": "#F8F8F2",
    "yellow": "#F1FA8C",
    "brightBlack": "#6272A4",
    "brightBlue": "#D6ACFF",
    "brightCyan": "#A4FFFF",
    "brightGreen": "#69FF94",
    "brightPurple": "#FF92DF",
    "brightRed": "#FF6E6E",
    "brightWhite": "#FFFFFF",
    "brightYellow": "#FFFFA5"
  }
],
```
[Colors scheme](https://draculatheme.com/windows-terminal)
> Original source of the tutorial [Blog Renato Groffe](https://renatogroffe.medium.com/dicas-de-visual-studio-code-integra%C3%A7%C3%A3o-com-git-via-terminal-e-kubernetes-templates-pt5-395819902ab7)