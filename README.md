### 1. [ Recommended apps ]

sudo pacman -S firefox libreoffice sshpass git powerprofilesctl flatpak openrgb zsh-autosuggestions zsh-syntax-highlighting spotify obsidian

yay -S vscodium warp-cli

#### oh my zsh kurulum komutu

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

<hr>

### 2. [ güç modunu değiştirme ] - (KDE VE GNOME için)

#### Servisi etkinleştir
sudo systemctl enable warp-svc <br>
sudo systemctl start warp-svc <br>

#### sonrasında şu komutları gir
(EKlencek...)

<hr>

### 3. powerprofilesctl kurulum ayarı

#### nano editörü ile .zshrc dosyasını düzenle ve bunları ekle (değiştireiblirsin)

##### komut yazarak direkt aktif hale getirebilirsin
alias pwrb='powerprofilesctl set balanced' <br>
alias pwrp='powerprofilesctl set performance' <br>
alias pwrs='powerprofilesctl set power-saver' <br>
alias pwrlist='powerprofilesctl list' <br>
alias pwrget='powerprofilesctl get' <br>

#### terminalde auto-complate ve syntax kontrolü yapan birkaç plugin .zshrc dosyasına ekle
source /usr/share/zsh/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh <br>
source /usr/share/zsh/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh <br>

#### Sonrasında şu komutu çalıştır
source ~/.zshrc

<hr>

### 4. [servisleri devre dışı bırakma - etkinleştirme ] - (Discord girmek isteyenler için)

alias dwarp='sudo systemctl disable warp-svc'
alias ewarp='sudo systemctl enable warp-svc'
