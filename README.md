# Mind-Network-Testnet-Ağı

![97393721](https://github.com/tuncgs52/mind-network-testnet/assets/80161670/1f233c77-d6b0-4ebd-9b48-a6b933affbbe)



# Mind Network Nedir?
Mind Network, Web3'teki tüm verilerinizi, akıllı sözleşmelerinizi ve yapay zekayı koruyan bir Sıfır Güven Veri Gölüdür.


# İşlemlere başlamadan Önce Metamask Cüzdanınızda Goerli Eth Olsun.

> ## [İlk Önce Twitteki Adımları Yapıyoruz](https://scan.mindnetwork.xyz/)



#  Bu işlemleri yaparken ben sunucu kullandım.
Gerekli Kütüphanleri İndiriyoruz.

```
sudo apt-get update && sudo apt-get upgrade
```

```
sudo apt-get install ca-certificates curl gnupg
```

```
apt install screen
```

```
sudo install -m 0755 -d /etc/apt/keyrings
```

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

```
sudo chmod a+r /etc/apt/keyrings/docker.gpg
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

![Ekran görüntüsü 2023-08-22 191631](https://github.com/tuncgs52/mind-network-testnet/assets/80161670/f7fe7ad9-8503-4a7b-8afd-d1a2d02f8051)


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

![Ekran görüntüsü 2023-08-22 194921](https://github.com/tuncgs52/mind-network-testnet/assets/80161670/aa6e9aba-597a-410f-83ad-a6eae1813f2c)


Tıklıyoruz Metamask açılacak bütün izinleri veriyoruz.

![Ekran görüntüsü 2023-08-22 195730](https://github.com/tuncgs52/mind-network-testnet/assets/80161670/e31f437b-8ffc-4ddb-9c4e-1dc53376c580)


Bütün işlemler başarılı olunca, Alttaki resim gibi gözükecek.

![Ekran görüntüsü 2023-08-22 195817](https://github.com/tuncgs52/mind-network-testnet/assets/80161670/bb4261c4-00c9-401c-b8e9-f712960d6f02)


İşlemleri yapmak benim çok hoşuma gitti. beğendiyseniz forklamayı unutmayın.




