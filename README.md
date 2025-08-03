# Arch Linux .zsahrc config ve gerekli uygulamalar

### 1. [ Recommended apps ]

sudo pacman -S firefox libreoffice sshpass git powerprofilesctl flatpak openrgb zsh-autosuggestions zsh-syntax-highlighting spotify obsidian

### 2. yay kurulum

git clone https://aur.archlinux.org/yay.git <br>

#### Dizine gir
cd yay

#### yay paketini derle ve kurmaya başla gelen cevaplara da Y de
makepkg -si

yay -S vscodium warp-cli

### 3. oh my zsh kurulum komutu

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

<hr>

### 4. [ güç modunu değiştirme ] - (KDE VE GNOME için)

<hr>

#### nano editörü ile .zshrc dosyasını düzenle ve bunları ekle (değiştireiblirsin)

### 5. CLoudflare warp kurulum ayarları

#### Servisi etkinleştir
sudo systemctl enable warp-svc <br>
sudo systemctl start warp-svc <br>

#### sonrasında şu komutları gir
(EKlencek...)

### 6. .zshrc eklemen gereken configler

#### autocomplate ve syntax yazım özelliği

source /usr/share/zsh/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh <br>
source /usr/share/zsh/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh <br>

#### Sonrasında şu komutu çalıştır
source ~/.zshrc <br>

#### Cloudflare warp servis ksıayol ile etkin-devre dışı yapma
alias dwarp='sudo systemctl disable warp-svc' <br>
alias ewarp='sudo systemctl enable warp-svc' <br>

#### powerprofilesctl komut kısayol atama
alias pwrb='powerprofilesctl set balanced' <br>
alias pwrp='powerprofilesctl set performance' <br>
alias pwrs='powerprofilesctl set power-saver' <br>
alias pwrlist='powerprofilesctl list' <br>
alias pwrget='powerprofilesctl get' <br>


