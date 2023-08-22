# Mind-Network-Testnet

mind network nedir?


# İlk önce node kurmanız lazım,

> ## [kurulum linki](https://github.com/brsbrc/Testnetler-ve-Rehberler/tree/main/Inery)
> 

# Görev 1: Master Node Kaydetme Kısmına kadar herşeyi yapın.


# screen içinde loglar akmaya başladıktan sonra 'CTRL a d' ile screenden çıkın



# İnery screenini Vs Silmeyin.


# 2-Ana ekranda, Terminalde

```
pkill nodine
```

# Diyoruz. loglar durdumu emin olmak için tekrar screene girip ister bakın ister bakmayın. Ana Ekrandan devam ediyoruz...

# Daha sonra

```
pidof nodine
```

# Dediğimizde tepki yoksa devam ediyoruz. Tepki varsa

```
pkill nodine
```

# birkaç kez tekrarlayın.


# 3-) Terminalde aşağıdaki linkten snapshotu indirin.


> ## [snapshot linki](https://snapshot.inery.io/)  sitesine girin “curl” ile başlayan “.bin” ile biten kodu sunucuya yapıştırın.


# Uzunca ismi olan snapshot dosyası inicek, ortalama 15mb olmasi gerek, wincp ile girip bakın. eğer doğru inmemişse, sayfayı yenileyip yenisini indirin.


# 4-)Daha Sonra uzunca ismi olan snapshots dosyasını wincp ile


inery-node/inery.setup/master.node/blockchain/data/snapshots


# Klasörünün içine atıyoruz.


# 5-)Daha sonra şu 2 klasörü silin,


```
cd
```

```
rm -r inery-node/inery.setup/master.node/blockchain/data/blockchain
```

```
rm -r inery-node/inery.setup/master.node/blockchain/data/state
```

# 6-) Terminale Giriyoruz.

```
cd inery-node/inery.setup/master.node
```

# içine giriyoruz.

```
nano snapshots.sh
```

# 7.adımdaki kodları düzenleyerek yapıştırıyoruz. degişecek 4 tane kod var.

HESAP_PUBLİC_KEY:HESAP_PRİVATE_KEY

SUNUCU_İP

HESAP_İSMİ

SNAPSHOT_İSMİ

# 7-) DEDİĞİM YERLERİ DÜZENLEYİN.

```
#!/bin/bash
DATADIR="./blockchain"
if [ ! -d $DATADIR ]; then
mkdir -p $DATADIR;
fi

nodine --snapshot $DATADIR"/data/snapshots/SNAPSHOT_İSMİ" \
--plugin inery::producer_plugin \
--plugin inery::producer_api_plugin \
--plugin inery::chain_plugin \
--plugin inery::chain_api_plugin \
--plugin inery::http_plugin \
--plugin inery::history_api_plugin \
--plugin inery::history_plugin \
--plugin inery::net_plugin \
--plugin inery::net_api_plugin \
--data-dir $DATADIR"/data" \
--blocks-dir $DATADIR"/blocks" \
--config-dir $DATADIR"/config" \
--access-control-allow-origin=* \
--contracts-console \
--http-validate-host=false \
--verbose-http-errors \
--p2p-max-nodes-per-host 100 \
--connection-cleanup-period 10 \
--master-name HESAP_İSMİ \
--http-server-address 0.0.0.0:8888 \
--p2p-listen-endpoint SUNUCU_İP:9010 \
--p2p-peer-address tas.blockchain-servers.world:9010 \
--signature-provider HESAP_PUBLİC_KEY=KEY:HESAP_PRİVATE_KEY \
--p2p-peer-address sys.blockchain-servers.world:9010 \
--p2p-peer-address master1.blockchain-servers.world:9010 \
--p2p-peer-address master2.blockchain-servers.world:9010 \
--p2p-peer-address master3.blockchain-servers.world:9010 \
>> $DATADIR"/nodine.log" 2>&1 & \
echo $! > $DATADIR"/ined.pid"
```

# Kaydedip Çıkın

# 8-) En son şu kodları girin. Terminalde

```
cd
```

```
cd inery-node/inery.setup/master.node
```


```
chmod +x snapshots.sh
```

```
cd; source .bashrc; cd -
```

```
./snapshots.sh
```


# Bunlarıda Girdikten Sonra

```
screen -r inery
```

# yazın Bloklara bakabilirsiniz esleşmesi 5dk sürer

# Bunlarıda Yaptıktan sonra Kurulum floodundaki, Hesap onaylama kısmından devam edin
