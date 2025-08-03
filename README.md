# Arch Linux .zshrc config ve kurulan uygulamalar

### 1. Recommended apps

sudo pacman -S firefox libreoffice git flatpak

### 2. yay kurulum

git clone https://aur.archlinux.org/yay.git <br>

#### 2.1 Dizine gir
cd yay

#### 2.2 yay paketini derle ve kurmaya başla gelen cevaplara da Y de
makepkg -si

#### arch reposunda bulunmadığı için yay dan indirilen apps (OPSİYONEL)
yay -S vscodium warp-cli

### 3. oh my zsh kurulum komutu

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

<hr>

### 4. CLoudflare warp kurulum ayarları

#### 4.1 Servisi etkinleştir
sudo systemctl enable --now warp-svc <br>

#### 4.2 Bu komutlar seni kaydeder ve Warp ağına bağlar.
warp-cli register <br>
warp-cli connect <br>

#### 4.3 warp ağında bağlı mısın bunu bir kontrol et.
warp-cli status

<hr>

### 5. .zshrc eklemen gereken configler. <br>

#### !!! shell olarak zsh kullanıyorsanız eğer bu ayarları yapın. !!!

#### autocomplate ve syntax yazım özelliği .zshrc ekle.

##### 5.1 kurulumu yap.
sudo pacman -S zsh-autosuggestions zsh-syntax-highlighting

##### 5.2 .zshrc dosyasına ekle.
source /usr/share/zsh/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh <br>
source /usr/share/zsh/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh <br>

##### 5.3 Sonrasında şu komutu çalıştır.
source ~/.zshrc <br>

<hr>

### 6. GÜç Planını Değiştirme

#### 6.1 powerprofilesctl kur.

sudo pacman -S powerprofilesctl

- powerprofilesctl get = mevcut kullandığın güç planını gösterir.
- powerprofilesctl set balanced = güc tasarrufunu dengeli olarak ayarlar.
- powerprofilesctl set performance = güç tasarrufunu performans olarak ayarlar.
- powerprofilesctl set power-saver = güç tasarrufunu pil ömrüne bağlı ayarlar **(Laptoplar için kullanılabilir)**

#### powerprofilesctl komut kısayol atamak istersen (OPSİYONEL)
alias pwrb='powerprofilesctl set balanced' <br>
alias pwrp='powerprofilesctl set performance' <br>
alias pwrs='powerprofilesctl set power-saver' <br>
alias pwrlist='powerprofilesctl list' <br>
alias pwrget='powerprofilesctl get' <br>

##### Hyperland ile kurmak isteyenler için

sudo pacman -S power-profiles-daemon


