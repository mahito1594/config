# My config files

## Summary
いくつかの設定ファイルをまとめたもの．
Emacs の設定ファイルは[こちら](https://github.com/mahito1594/dotemacs)．

```
$ git clone --recursive git@github.com:mahito1594/config.git ~/projects/config
```

## Git
git のエイリアスをまとめたもの．
macOS の場合

```
$ cd ~/projects/config/git
$ mkdir -p ~/.config
$ ln -s ~/projects/config/git/ ~/.config/git
$ git config --global include.path "~/.config/git/aliases"
```
などとする．

global な gitignore の設定は

```
$ gibo dump macOS >> ~/.gitignore_global
$ git config --global core.excludesfile "~/.gitignore_global"
```

などとする． [gibo](https://github.com/simonwhitaker/gibo) コマンドの代わりに [gitignore.io](http://gitignore.io/) を利用してもよい．

## nano
簡単な nano の設定．
シンタックスハイライトに https://github.com/scopatz/nanorc を利用している．

```
$ mkdir -p ~/.config ~/projects/config/nano/backups
$ ln -s ~/projects/config/nano/ ~/.config/nano
```
