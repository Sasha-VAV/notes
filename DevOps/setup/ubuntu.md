# Ubuntu setup

### zsh
```shell
chsh -s $(which zsh)
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
vim .zshrc
source .zshrc
```
- theme
```shell
p10k

```
plugins
```
plugins=(
  git          # Git shortcuts (e.g., `gb` for `git branch`)
  zsh-autosuggestions  # Suggests commands as you type
  zsh-syntax-highlighting  # Colors commands for validity
  sudo         # Double-press ESC to add `sudo`
  docker       # Docker completions
)
```

### uv
- installation
- zsh autocomplete
```shell
echo 'eval "$(uv generate-shell-completion zsh)"' >> ~/.zshrc
```
- Some text next
- 