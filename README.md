# nerdy-setup-osx
Repository containing dotfiles and recommended setup instructions for development on Mac OS.


## iTerm
1. Install [iTerm](https://www.iterm2.com/)
2. Install [solarized](http://ethanschoonover.com/solarized)
3. Open iTerm2 and setup solarized as default theme
4. Customise your default font (optional):
    - Install [SourceCode Pro](https://github.com/adobe-fonts/source-code-pro) or the one you prefer.
    - Setup ad default in iTerm configuration menu.

## Bash Profile

```
$ ln -s /path/to/nerdy-setup-osx/.vim ~/.vim
$ git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
$ vim
$ :PluginInstall
```

## Vim

Why aren't you coding with Vim? Vim is the One True Editor. Repent and save yourselves.

```
$ ln -s /path/to/nerdy-setup-osx/.bash_profile ~/.bash_profile
$ source ~/.bash_profile
```

## Fish
1. Install [Fish](http://fishshell.com/)
2. Install [Oh My Fish](https://github.com/bpinto/oh-my-fish)
```
$ git clone git://github.com/bpinto/oh-my-fish.git ~/.oh-my-fish
$ cp ~/.oh-my-fish/templates/config.fish ~/.config/fish/config.fish
```
3. Run `$ fish` to switch from bash to fish


## Homebrew

Install [Homebrew](http://brew.sh). It's awesome!

```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Node.js

1. Install [nvm](https://github.com/creationix/nvm). Run `$ brew install nvm`.

2. Install Node.js and io.js  

```
$ nvm install node stable
$ nvm install iojs latest

# make iojs default
$ nvm alias default iojs latest
```
