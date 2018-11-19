# .zshrc
An easy to configure .zshrc file with 256 color support, github status, program exit status, directory truncation, and sane defaults.  The `~/.zsh_aliases` file is also included with some useful aliases and functions (which can be ran just like a normal command).

# Configuration
On first run, `~/.zsh_prompt.conf` will be created.  This file contains all of the configuration options for the zsh prompt.  Color options may be previewed with `prompt_fg_samples` and `prompt_bg_samples`.

![config](https://ibin.co/4N7DicoelURE.png)

If you wish to change the contents of the prompt, the `PS1` variable in the `~/.zshrc` file must be edited (I tried to make this a config option, but it breaks directory truncation :( ).  The three functions listed below are custom functions included in this .zshrc file.  Everything else is done with zsh's prompt expansion.  See [the zsh website](http://zsh.sourceforge.net/Doc/Release/Prompt-Expansion.html#Prompt-Expansion) for details on prompt expansion.

```bash
### SET THE PROMPT ###
# set the contents of the prompt
# '%$(MAIN_COLOR)F' is the color based on the $PWD as set in ~/.zsh_prompt.conf
# '%{$(BACKGROUND_COLOR)%}' is the background color as set in ~/.zsh_prompt.conf
# '$(DIR_TRUNCATED)' is a function in this .zshrc which truncates long directories in the prompt
# see http://zsh.sourceforge.net/Doc/Release/Prompt-Expansion.html#Prompt-Expansion for more info
PS1='%{$(BACKGROUND_COLOR)%}%$(MAIN_COLOR)F %n %S$(DIR_TRUNCATED)%s%k%f '
```

# Screenshots

Example setup:

![screenshot1](https://ibin.co/4N7CWd5H8BkO.png)

`~/.zsh_aliases` file:

![screenshot2](https://ibin.co/4N7Gxh3fPJMI.png)