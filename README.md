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

## GnuPG
`~/.gnupg` 以下にシンボリックリンクを貼るなどして利用する．
環境変数 `GPG_TTY` を正しく設定してやる必要がある．

```
$ export GPG_TTY=$(tty)
# or echo 'GPG_TTY=$(tty)' >> ~/.bash_profile (or ~/.bashrc)
```

詳しくは [Commonly seen problems](https://www.gnupg.org/documentation/manuals/gnupg/Common-Problems.html) を参照．

## nano
簡単な nano の設定．
シンタックスハイライトに https://github.com/scopatz/nanorc を利用している．

```
$ mkdir -p ~/.config ~/projects/config/nano/backups
$ ln -s ~/projects/config/nano/ ~/.config/nano
```


## cmus/rc
[cmus](https://cmus.github.io/ "C* Music Player") の設定．
デフォルトだと vim 風のキーバインドなのでいくつか Emacs 風に置き換えている．

```
ln -s /path/to/mahito1594/cmus/ ${XDG_CONFIG_HOME}/cmus
```

cmus は以下の順に設定ファイルを読み込む:

1. `${XDG_CONFIG_HOME}/cmus/autosave`
1. 上が存在しない場合 `/usr/share/cmus/rc`
1. `{$XDG_CONFIG_HOME}/cmus/rc`

## Bash
### aliases
alias をまとめたもの

``` shell
echo 'source /path/to/config/bash/aliases' >> ~/.bash_profile
```

