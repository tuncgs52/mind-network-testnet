# Mind-Network-Testnet-Ağı

![97393721](https://github.com/tuncgs52/mind-network-testnet/assets/80161670/9c2c95ca-1512-4265-9dfd-a27214fcbc51)


# Mind Network Nedir?
Mind Network, Web3'teki tüm verilerinizi, akıllı sözleşmelerinizi ve yapay zekayı koruyan bir Sıfır Güven Veri Gölüdür.


# İşlemlere başlamadan Önce Metamask Cüzdanınızda Goerli Eth Olsun.

> ## [İlk Önce Twitteki Adımları Yapıyoruz](https://scan.mindnetwork.xyz/)



#  Bu işlemleri yaparken ben sunucu kullandım.
Gerekli Kütüphanleri İndiriyoruz.

```
sudo apt-get update && sudo apt-get upgrade
sudo apt-get install ca-certificates curl gnupg
apt install screen
```

```
sudo install -m 0755 -d /etc/apt/keyringscurl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpgsudo chmod a+r /etc/apt/keyrings/docker.gpg
```

```
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

# Nvm İndiriyoruz.

```
sudo apt install curl 
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash 
```

```
source ~/.bashrc
```

```
nvm install node
```

```
nvm install 16
```

```
nvm use 16
```

```
node -v
```

# Repoyu Klonluyoruz.
```
git clone https://github.com/mind-network/mind-lake-sdk-typescript.git
```

klasörün içine giriyoruz.

```
cd mind-lake-sdk-typescript/examples/src
```

Dosyamızın ismini değiştiriyoruz.

```
mv myconfig_template.ts myconfig.ts
```

Dosyamızın içine twitteki acces keyi giriyoruz.

```
nano myconfig.ts
```


Twitteki adımdaki acceskey'i resimdeki "YOUR_APP_KEY=" kısmına yapıştırıyoruz. CTRL, X, Y, ENTER Diyerek kaydediyoruz.

![Ekran görüntüsü 2023-08-22 191631](https://github.com/tuncgs52/mind-network-testnet/assets/80161670/8af304e4-4211-4e63-a93e-3b3a78fe0072)

# Yeni bir pencere açıyoruz.

```
screen -S mind
```

Klasörün içine giriyoruz.

```
cd
cd mind-lake-sdk-typescript/examples
```

```
npm install
```

2, 3dk bekliyoruz.

```
npm run start
```

Resimdeki gibi "http://sunucuip:8000" kopyalıyoruz ve metamaskın olduğu tarayıcıya yapıştırıyoruz. Vpn bağlı olmayın girmez.

![Ekran görüntüsü 2023-08-22 194921](https://github.com/tuncgs52/mind-network-testnet/assets/80161670/8075ef79-5e73-497f-85a5-c62e85017e58)

Tıklıyoruz Metamask açılacak bütün izinleri veriyoruz.

![Ekran görüntüsü 2023-08-22 195730](https://github.com/tuncgs52/mind-network-testnet/assets/80161670/0add9ecb-404f-4b59-948c-089d7559027c)

Bütün işlemler başarılı olunca, Alttaki resim gibi gözükecek.

![Ekran görüntüsü 2023-08-22 195817](https://github.com/tuncgs52/mind-network-testnet/assets/80161670/2c5242d7-e112-4be1-859f-0b1a3a06dd5f)

İşlemleri yapmak benim çok hoşuma gitti. beğendiyseniz forklamayı unutmayın.




