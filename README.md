# nerdy-setup-osx
Repository containing dotfiles and recommended setup instructions for development on Mac OS.


## iTerm

1. Install [iTerm](https://www.iterm2.com/)
2. Install [solarized](http://ethanschoonover.com/solarized)
3. Open iTerm and setup solarized as default theme
4. Customise your default font (optional):
    - Install [SourceCode Pro](https://github.com/adobe-fonts/source-code-pro) or the one you prefer
    - Setup ad default in iTerm configuration menu


## Homebrew

Install [Homebrew](http://brew.sh). It's awesome!

```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```


## Vim

Why aren't you coding with Vim? Vim is the One True Editor. Repent and save yourselves.

```
$ ln -s /path/to/nerdy-setup-osx/.vim ~/.vim
$ git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim

# Open vim
$ vim
 ```
Run `:PluginInstall` into vim command line.


## Bash Profile

```
$ ln -s /path/to/nerdy-setup-osx/.bash_profile ~/.bash_profile
$ source ~/.bash_profile
```


## Tmux

Tmux is a terminal multiplexer. It lets you switch easily between several programs in one terminal.

### Install with Homebrew
```
$ brew install tmux
```

### Build tmux from a release tarball
```
# Install wget if you didn't before
$ brew install wget

# Download tmux release tarball
$ wget http://downloads.sourceforge.net/project/tmux/tmux/tmux-2.0/tmux-2.0.tar.gz?r=&ts=1432285840&use_mirror=freefr tmux

# Configure, make and install
$ cd tmux && ./configure && make
$ sudo make install
```

### Build the latest from version control
```
# Clone tmux source code
$ git clone git://git.code.sf.net/p/tmux/tmux-code tmux-tmux-code  tmux
$ tmux

# Configure, make and install
$ sh autogen.sh
$ ./configure && make
```


## Fish

1. Install [Fish](http://fishshell.com/)
2. Install [Oh My Fish](https://github.com/bpinto/oh-my-fish)
3. Start / Restart fish

```
# This will install Oh My Fish
$ git clone git://github.com/bpinto/oh-my-fish.git ~/.oh-my-fish
$ mkdir ~/.config && mkdir ~/.config/fish
$ cp ~/.oh-my-fish/templates/config.fish ~/.config/fish/config.fish

# This will start fish
$ fish
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


## Octave

Install `Xcode` and the `Command Line Tools`. Once you’ve installed Xcode, you can install Command Line Tools in `Xcode > Preferences > Downloads`.

Download and install [XQuartz](https://xquartz.macosforge.org/landing/), so go ahead and download and install that now.

Download and install [AquaTerm](http://sourceforge.net/projects/aquaterm/?source=typ_redirect).

Download and install [Octave](http://sourceforge.net/projects/octave/?source=typ_redirect).

Next, open up a Terminal and do the following:
```
# Change `x.x.x` with your actual octave version
$ sudo ln -sf /usr/local/octave/x.x.x/bin/octave-x.x.x /usr/local/bin/octave
$ brew reinstall gnuplot --with-aquaterm --with-x11
$ ln -s ~/nerdy-setup-osx/.octaverc ~/.octaverc
```
