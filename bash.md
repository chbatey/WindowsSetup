## Vim mode with indicator

Required bash 4.4

In .inputrc

```
set show-mode-in-prompt on
set vi-ins-mode-string \1\e[34;1m\2(ins)\1\e[0m\2
set vi-cmd-mode-string \1\e[35;1m\2(cmd)\1\e[0m\2
# want vi to be the default editor for readline
set editing-mode vi

# vi settings
$if mode=vi
    # normal mode
    set keymap vi-command
    # insert mode
    set keymap vi-insert
    "jk": vi-movement-mode 
$endif
```

In .bash_profile


```
set -o vi
PS1=" \e[0;36m\u@\h \w> \e[m"
```

## Cygwin

### Explorer windows here function

```
exp() {
  /cygdrive/c/Windows/explorer.exe /e,`cygpath -w "$PWD"`
}
```

