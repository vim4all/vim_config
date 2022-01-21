# My vim config
My neovim configuration for Windows.
It is mosly used for:
- Python programming
- C programming
- Writing Latex documents

***

## Plugins

### Files and code navigation
1. **nerdtree** - file tree
1. **vim-nerdtree-tabs** tabs
1. **tagbar** - tags
1. **minimap** - minimap of code

### Style
1. **onedark** - color theme
1. **lightline** - 
1. **vim-devicons** - pictograms
1. **vim-rainbow** - brackets colors
1. **identLine** - scopes lines

### Code/text analysis and autocomplete
1. **vim-gitgutter** - git support
1. **vim-gramous** - grammar check (TO TEST)
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

``` flowchart
st=>start: Start|past:>http://www.google.com[blank]
e=>end: End|future:>http://www.google.com
op1=>operation: My Operation|past
op2=>operation: Stuff|current
sub1=>subroutine: My Subroutine|invalid
cond=>condition: Yes
or No?|approved:>http://www.google.com
c2=>condition: Good idea|rejected
io=>inputoutput: catch something...|future

st->op1(right)->cond
cond(yes, right)->c2
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)
```
