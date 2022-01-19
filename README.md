# My vim config
My neovim configuration.

***

## Plugins

### Files and code navigation
1. *nerdtree* - file tree
1. *vim-nerdtree-tabs* tabs
1. *tagbar* - tags
1. *minimap* - minimap of code

### Style
1. *onedark* - color theme
1. *lightline* - 
1. *vim-devicons* - pictograms
1. *vim-rainbow* - brackets colors
1. *identLine* - scopes lines

### Code/text analysis and autocomplete
1. *vim-gitgutter* - git support
1. *vim-gramous* - grammar check (TO TEST)
1. *vimspector* - debugger
1. *coc* - autocomplete (used for C and Python)

### Specific language related 
1. *vim-javascript* - javascript identation and etc
1. *vimtex* - plugin for latex
1. *vim-octave* - octave identation and etc

### Other
1. *md-img-paste* - images paste
1. *vim-pythonx*
1. *vim-wakatime* - programming monitor

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
'''
