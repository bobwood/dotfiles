# dotfiles
basic dotfiles

```bash
git clone --separate-git-dir=$HOME/.myconf https://github.com/bobwood/dotfiles.git $HOME/myconf-tmp
rsync -rv --exclude '.git' $HOME/myconf-tmp/ $HOME/
rm -r $HOME/myconf-tmp/
alias myc='/usr/bin/git --git-dir=$HOME/.myconf/ --work-tree=$HOME'
myc config status.showUntrackedFiles no
myc remote set-url origin git@github.com/bobwood/dotfiles.git
```
