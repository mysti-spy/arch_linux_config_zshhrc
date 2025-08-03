# Arch Linux .zsahrc config ve gerekli uygulamalar

### 1. Recommended apps

sudo pacman -S firefox libreoffice sshpass git powerprofilesctl flatpak spotify obsidian

### 2. yay kurulum

git clone https://aur.archlinux.org/yay.git <br>

#### 2.1 Dizine gir
cd yay

#### 2.2 yay paketini derle ve kurmaya başla gelen cevaplara da Y de
makepkg -si

#### arch reposunda bulunmadığı için yay dan indirilen apps (Opsiyonel)
yay -S vscodium warp-cli

### 3. oh my zsh kurulum komutu

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

<hr>

#### nano editörü ile .zshrc dosyasını düzenle ve bunları ekle (değiştireiblirsin)

### 5. CLoudflare warp kurulum ayarları

#### 5.1 Servisi etkinleştir
sudo systemctl enable --now warp-svc <br>

#### 5.2 Bu komutlar seni kaydeder ve Warp ağına bağlar.
warp-cli register <br>
warp-cli connect <br>

#### 5.3 warp ağında bağlı mısın bunu bir kontrol et.
warp-cli status

<hr>

### 6. .zshrc eklemen gereken configler.

#### autocomplate ve syntax yazım özelliği .zshrc ekle.

##### 6.1 kurulumu yap.
sudo pacman -S zsh-autosuggestions zsh-syntax-highlighting

##### 6.2 .zshrc dosyasına ekle.
source /usr/share/zsh/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh <br>
source /usr/share/zsh/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh <br>

##### 6.3 Sonrasında şu komutu çalıştır.
source ~/.zshrc <br>

#### Cloudflare warp servis ksıayol ile etkin-devre dışı yapma (Opsiyonel)
alias dwarp='sudo systemctl disable warp-svc' <br>
alias ewarp='sudo systemctl enable warp-svc' <br>

##### güç modunu değiştirme - (KDE VE GNOME için)

sudo pacman -S powerprofilesctl

- powerprofilesctl get = mevcut kullandığın güç planını gösterir.
- powerprofilesctl set balanced = güc tasarrufunu dengeli olarak ayarlar.
- powerprofilesctl set performance = güç tasarrufunu performans olarak ayarlar.
- powerprofilesctl set power-saver = güç tasarrufunu pil ömrüne bağlı ayarlar **(Laptoplar için kullanılabilir)**

#### powerprofilesctl komut kısayol atama
alias pwrb='powerprofilesctl set balanced' <br>
alias pwrp='powerprofilesctl set performance' <br>
alias pwrs='powerprofilesctl set power-saver' <br>
alias pwrlist='powerprofilesctl list' <br>
alias pwrget='powerprofilesctl get' <br>

##### Hyperland isteyenler için

sudo pacman -S power-profiles-daemon


