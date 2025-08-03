### Recommended apps

sudo pacman -S firefox libreoffice sshpass git powerprofilesctl flatpak openrgb zsh-autosuggestions zsh-syntax-highlighting

yay -S vscodium (none telemetry)

#### oh my zsh kurulum komutu

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

### güç modunu değiştirme (powerprofilesctl)

alias pwrb='powerprofilesctl set balanced'
alias pwrp='powerprofilesctl set performance'
alias pwrs='powerprofilesctl set power-saver'
alias pwrlist='powerprofilesctl list'
alias pwrget='powerprofilesctl get'

### yunohost sunucusuna erişme (Self-host kullananlar için OPSİYONEL)

alias mys='sshpass -p "password" ssh ssh_bilgilerin'

source /usr/share/zsh/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh
source /usr/share/zsh/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh

### servisleri devre dışı bırakma - etkinleştirme

#### warp dns servisini aç-kapa
alias dwarp='sudo systemctl disable warp-svc'
alias ewarp='sudo systemctl enable warp-svc'
