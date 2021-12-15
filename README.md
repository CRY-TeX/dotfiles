# dotfiles
linux configuration files

Credit to: https://www.ackama.com/what-we-think/the-best-way-to-store-your-dotfiles-a-bare-git-repository-explained/

Storing your dotfiles using a non-bare, default repository:
1. git init $HOME/.cfg
2. alias config='/usr/bin/git --git-dir=$HOME/.cfg/.git/ --work-tree=$HOME'
3. echo "alias config='/usr/bin/git --git-dir=$HOME/.cfg/.git/ --work-tree=$HOME'" >> $HOME/.zsh/aliases
4. config config --local status.showUntrackedFiles no
5. config add .vimrc + config commit -m "add .vimrc" + Set up a remote repository on GitHub or your Git server of choice + config push

Installing:
1. echo ".cfg" >> .gitignore
2. git clone <remote-git-repo-url> $HOME/.cfg
3. alias config='/usr/bin/git --git-dir=$HOME/.cfg/.git --work-tree=$HOME'
4. config config --local status.showUntrackedFiles no
5. config checkoutUsing a bare repository like @durdn’s tutorial
1. git init --bare $HOME/.cfg
2. alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
3. echo "alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'" >> $HOME/.zsh/aliases
4. config config --local status.showUntrackedFiles no
5. config add .vimrc + config commit -m "add .vimrc" + set up a remote repository on GitHub or your Git server of choice + config push

Installing:
1. echo ".cfg" >> .gitignore
2. git clone --bare <remote-git-repo-url> $HOME/.cfg
3. alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'
4. config config --local status.showUntrackedFiles no
5. config checkoutNow for the line by line breakdown. But first . . .
