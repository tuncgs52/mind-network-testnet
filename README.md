# Mind-Network-Testnet-Ağı

# Mind Network Nedir?
Mind Network, Web3'teki tüm verilerinizi, akıllı sözleşmelerinizi ve yapay zekayı koruyan bir Sıfır Güven Veri Gölüdür.

İşlemlere başlamadan Önce Metamask Cüzdanınızda Goerli Eth Olsun.

> ## https://scan.mindnetwork.xyz/






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






