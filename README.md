dotfiles
===================

Local dotfiles for use with
[thoughbot dotfiles](https://github.com/thoughtbot/dotfiles)

Requirements
------------

Set zsh as your login shell:

    chsh -s $(which zsh)

Install
-------

Install Inconsolata-dz for Powerline

    brew tap caskroom/fonts
    brew cask install font-inconsolata-dz-for-powerline

Install [rcm](https://github.com/thoughtbot/rcm):

    brew tap thoughtbot/formulae
    brew install rcm

Clone this repo:

    git clone git://github.com/jsntv200/dotfiles.git ~/.dotfiles

Clone [thoughbot dotfiles](https://github.com/thoughtbot/dotfiles):

    git clone git://github.com/thoughtbot/dotfiles.git ~/.dotfiles-thoughtbot

Clone [antigen](https://github.com/zsh-users/antigen) for installing zsh plugins:

    git clone https://github.com/zsh-users/antigen.git ~/.antigen

Install the dotfiles:

    env RCRC=$HOME/.dotfiles/rcrc rcup

After the initial installation, you can run `rcup` without the one-time variable
`RCRC` being set (`rcup` will symlink the repo's `rcrc` to `~/.rcrc` for future
runs of `rcup`). [See
example](https://github.com/thoughtbot/dotfiles/blob/master/rcrc).

You should run `rcup` after pulling a new version of the repository to symlink
any new files in the repository.

Additional Installs
-------

Install Neovim to get full 256 color support

    brew tap neovim/homebrew-neovim
    brew install --HEAD neovim

Update iTerm2 to the latest release

    brew tap caskroom/versions
    brew cask install iterm2-nightly
