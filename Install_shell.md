# Customize SHELL with zsh (Oh-My-Zsh)

- [x] [Install ZSH shell](#install-zsh-shell)
- [x] [Install Oh-My-Zsh](#install-oh-my-zsh)
  - [x] For current user
  - [x] For root user
- [x] [Configuration .zshrc file](#configuration-zshrc-file)

</br>

---

</br>

## Install ZSH shell

- Bashrc အစား ZSH ကိုပြောင်းသုံးပါမယ်။ ဘာလို့ဆို Terminal လှတာလေးသုံးခြင်လို့ပါ :)

</br>

```bash
# Install zsh
sudo apt install -y zsh

# Check zsh version
zsh --version

# Make ZSH your default shell
chsh -s /usr/bin/zsh
```

</br>

---

</br>



## Configuration .zshrc file

- [x] [Change Theme ` robbyrussell ` to ` agnoster `](#change-theme)
- [x] [Add some official supported plugins](#add-some-official-supported-plugins)
- [x] [Download and install some third party plugins](#download-and-install-some-third-party-plugins)

</br>

### Change Theme

</br>

- Change Theme ` robbyrussell ` to ` agnoster `

</br>

> **For current user:**

</br>

- Open `.zshrc` file with nano:

```bash
nano ~/.zshrc
```

- Find `ZSH_THEME="robbyrussell"`

- Change to `ZSH_THEME="agnoster"`

- Use `Ctrl-O` to save.

- Use `Ctrl-M` to format.

- And `Ctrl-X` to exit.

</br>

- Update `.zshrc` file

```bash
source ~/.zshrc
```

</br>

> **For root user:**

</br>

- Open `.zshrc` file with nano:

```bash
sudo su

nano /root/.zshrc

```

- Find `ZSH_THEME="robbyrussell"`

- Change to `ZSH_THEME="agnoster"`

- Use `Ctrl-O` to save.

- Use `Ctrl-M` to format.

- And `Ctrl-X` to exit.

</br>

- Update `.zshrc` file

```bash
source /root/.zshrc

exit
```

</br>

### Add some official supported plugins

</br>

> #### For current User

</br>

- We will be add git, gitignore, laravel, node, npm, heroku, python, django, vscode and yarn

- > You can checkout more plugin in 👉️ [HERE](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins) 👈️

</br>

- open .zshrc
  
```bash
nano ~/.zshrc
```

- Find `plugins=(git)`
- Add more plugins
  - `plugins=(git gitignore laravel node npm heroku python vscode yarn)`
- Use `Ctrl-O` to save.

- Use `Ctrl-M` to format.

- And `Ctrl-X` to exit.

</br>

- Update `.zshrc` file

```bash
source ~/.zshrc
```

</br>

> #### For root User

</br>

- open .zshrc
  
```bash
sudo su

nano /root/.zshrc
```

- Find `plugins=(git)`
- Add more plugins
  - `plugins=(git gitignore laravel node npm heroku python vscode yarn)`
- Use `Ctrl-O` to save.

- Use `Ctrl-M` to format.

- And `Ctrl-X` to exit.

</br>

- Update `.zshrc` file

```bash
source /root/.zshrc
```

</br>

## Download and install some third party plugins

</br>

- We will be install `autojump, syntax-highlighting, autosuggestions, zsh-completions` and `history-substring-search`

</br>

### Install `autojump`

</br>

```bash
cd ~

# Install autojump
git clone git://github.com/wting/autojump.git

cd autojump

# Install 
./install.py or ./uninstall.py

# Open .zshrc file and paste the below cmd:
sudo nano ~/.zshrc

```

- > Copy the following command and paste in the end of .zshrc file

```bash
[[ -s /home/killer/.autojump/etc/profile.d/autojump.sh ]] && source /home/killer/.autojump/etc/profile.d/autojump.sh

autoload -U compinit && compinit -u
```

- Save and exit file.

</br>

### Install `zsh-syntax-hightlighting`

</br>

```bash
cd ~

# Install zsh-syntax-hightlighting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# Add zsh-syntax-highlighting to plugins
sudo nano ~/.zshrc
```

- Add `zsh-syntax-highlighting` in plugins. Eg- `plugins=(...other zsh-syntax-highlighting)`

- Save and exit file.
  
</br>

### Install zsh-autosuggestions

</br>

```bash
cd ~

# Install zsh-completions
git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions

# Add zsh-completions to plugins
sudo nano ~/.zshrc

```

- Add `zsh-completions` in plugins. Eg- `plugins=(...other zsh-completions)`

- Save and exit file.

</br>

### Install zsh-completions

</br>

```bash
cd ~

# Install zsh-completions
git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions

# Add zsh-completions to plugins
sudo nano ~/.zshrc

```

- Add `zsh-completions` in plugins. Eg- `plugins=(...other zsh-completions)`

- Save and exit file.
  
</br>

### Install zsh-history-substring-search

</br>

```bash
cd ~

# Install zsh-history-substring-search
 git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search

# Add zsh-history-substring-search to plugins
sudo nano ~/.zshrc

```

- Add `zsh-history-substring-search` in plugins. Eg- `plugins=(...other zsh-history-substring-search)`

- Save and exit file.
  
</br>

All finished. Refresh the .zshrc file

```bash
source ~/.zshrc
```

---
