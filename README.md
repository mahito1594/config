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
$ curl -sL https://www.gitignore.io/api/osx >> gitignore_global
$ mkdir -p ~/.config
$ ln -s ~/projects/config/git/ ~/.config/git
$ git config --global core.excludefile ~/.config/git/gitignore_global
$ git config --global include.path "~/.config/git/aliases"
```
とする．

## nano
簡単な nano の設定．
シンタックスハイライトに https://github.com/scopatz/nanorc を利用している．

```
$ mkdir -p ~/.config ~/projects/config/nano/backups
$ ln -s ~/projects/config/nano/ ~/.config/nano
```
