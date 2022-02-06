# My vim config
Моя конфігурація Neovim для Windows.
Використовується переважно для:
- Програмування на мовах C, Python, JavaScript
- Написаня документів Latex
- Редагування Markdown, HTML

My neovim configuration for Windows.
It is mosly used for:
- Python, C, JavaScript programming
- Writing Latex documents
- Markdown, HTML editing

***

## Плагіни \ Plugins

### Files and code navigation
1. **nerdtree** - дерево файлів \ file tree
1. **vim-nerdtree-tabs** tabs
1. **tagbar** - теги \ tags
1. **minimap** - minimap of code

### Style
1. **onedark** - кольорова схема \ color theme
1. **lightline** - 
1. **vim-devicons** - піктограми \ pictograms
1. **vim-rainbow** - підсвічування дужок \ brackets colors
1. **identLine** - scopes lines

### Code/text analysis and autocomplete
1. **vim-gitgutter** - підтримка git \ git support
1. **vim-gramous** - перевірка граматики \ grammar check (TO TEST)
1. **vimspector** - debugger
1. **coc** - autocomplete (used for C and Python)

### Specific language related 
1. **vim-javascript** - javascript identation and etc
1. **vimtex** - plugin for latex
   - Used *MiKTeX* compiler
   - *SumatraPDF* is used to view documents
1. **vim-octave** - octave identation and etc
1. **markdown-preview** - markdown preview

### Other
1. **md-img-paste** - images paste
1. **vim-pythonx**
1. **vim-wakatime** - programming monitor

***

## Specific configs

### vimspector config for C language

File **.vimspector.json**

```json
 {
   "configurations": {
     "FinMat": {
      "adapter": "vscode-cpptools",
      "configuration": {
        "type": "cppdbg",
        "request": "launch",
        "program": "${workspaceRoot}/out/mpc_c.exe",
        "args": [],
        "cwd": "${workspaceRoot}",
        "environment": [
          { "name": "VIMRUNTIME", "value": "${workspaceRoot}" }
        ],
        "externalConsole": false,
        "stopAtEntry": true,
        "MIMode": "gdb",
        "setupCommands": [
            {
                "description": "Enable pretty-printing for gdb",
                "text": "-enable-pretty-printing",
                "ignoreFailures": true
            }
        ],
        "logging": {
          "engineLogging": false
        }
      }
    }
  }
}
```
