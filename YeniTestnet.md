<h1 align="center">Fleek Network</h1>


> Hocam Fleek testneti ne kadar sürecek? - Cevabı [burada.](https://blog.fleek.network/post/fleek-network-testnet-phase0/)

> Hocam ödüllü mü? - Cevabı [burada.](https://blog.fleek.network/post/fleek-network-testnet-plans/)

> Arkadaşlar ricamdır şunla şu yan yana kurulurmu sorusunu artık sormayın.

> Topluluk kanalları: [Duyurular](https://t.me/RuesAnnouncement) - [Sohbetler](https://t.me/RuesChat) - [Discord](https://discord.gg/V2rX68cy)

<h1 align="center"> Donanım </h1>

> Kendim kurduğum donanım, [Hetzner](https://hetzner.cloud/?ref=gIFAhUnYYjD3) kullandım.

> Sunucu şifrenizi unutmayın, Fleek'ten kaynaklanan bir bugdan ötürü `qemu-guest` siliniyor ve şifre yenileyemiyorsunuz.

```console
# Ubuntu 22.04 şart. 
4 CPU 8 RAM
```

> user ekleyin
```console
# sinanEngin yazan yerleri değişin.
adduser sinanEngin
usermod -aG sudo sinanEngin
su sinanEngin
cd /home/sinanEngin
```

<h1 align="center"> Kurulum </h1>

```console
# Güncellemelerimiz
sudo apt update && sudo apt upgrade -y

sudo fallocate -l 10240M /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile

# rust ve kütüphaneleri yüklüyoruz seçeneklerde 1'i seçiyoruz:
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
rustup update
```

```console
# Script ile kuruyoruz aşamalar çok uzun sürebilir, sunucu performansınıza bağlı.
curl https://get.fleek.network | bash
# Yes/No sorularına yes diyoruz

# bize kurulum tamamlanınca Node Public Key ve Consensus Public Key vericek kaydedin.
```

> Bu esnada [buradan](https://faucet.testnet.fleek.network/) token alın fleeke cüzdan açıp

```console
# Servisi başlatalım. Tek Tek girin
sudo systemctl start lightning.service
sudo systemctl stop lightning.service
sudo systemctl restart lightning.service
```

> Mint ettiğiniz yerden bilgileri girip işlemi tamamlayın.

> kontrol komutu: `curl -sS https://get.fleek.network/healthcheck | bash`

![image](https://github.com/ruesandora/Fleek/assets/101149671/50a26d0c-d44f-4c61-8454-1e19d5f1890b)




