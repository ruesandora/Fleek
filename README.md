## <h1 align="center">Fleek Network</h1>
![image](https://user-images.githubusercontent.com/101149671/209468276-05345f01-8643-4a57-8109-77d24ba8f622.png)


## Notlar ve okunması gerekenler:
 
* Testnet `ödüllü değil`. Ödüllüsü daha sonra başlayacak.
* Neden kuralım? Sunucuz boştadır, hiç bir işe yaramıyordur, oyalanmak veya öğrenmek istiyorsunuzdur.
* Gidip para verip sunucu almayın. Burada yaşadığınız sorunları araştırarak öğrenin.
* Eğer kendi aranızda Fleek hakkında sohbet etmek isterseniz [Link](https://t.me/FleekNetworkTurkish)
* Özellikle bu testnette alacağınız sorunları kendinizin çözmesini istiyorum. Zaten ödüllü değil, bir aceleniz yok.. sabırla.
* Son olarak kurulum esnasında bir çok kez `y/n` seçeneği çıkacak, `y + enter` ile geçiyoruz.
* Fleek Network 25 Milyon$ yatırım aldı.
* Fleek'in port numarası: `4069`

## Gereksinimler:

* Boşta olan sunucunuz bu donanıma sahip olmasa bile kurulum yapın.
* Yüksek ihtimal hata alınacak durumlar olabilir, ama çözülür.
* RAM için yer açmak isterseniz: [Link](https://github.com/ruesandora/swap-space/blob/main/README.md)
```
4 CPU 
4 RAM
```

## Kurulum:
```
sudo su
```
```
sudo apt update && sudo apt upgrade
```
```
sudo apt install screen curl tar wget jq build-essential
```
```
sudo apt install make clang pkg-config libssl-dev cmake
```
```
sudo apt install curl build-essential gcc make
```

## rustup'u kuruyoruz:

* Eğer `Ziesha` sunucunuza kuruyorsanız ve silmediyseniz yüklüdür zaten
* `ls -a` ile kontrol edebilirsiniz (`.rustup`)
* Sadece `curl` komutunu girmeyin.
* rustup'u ilk defa kuruyorsanız 1-2-3 diye seçenek geldiğinde 1'i seçin.
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
```
source ~/.profile
source ~/.cargo/env
```

## sccache ve protobufer'i kuruyoruz:

* Yüklemesi biraz uzun sürebileceği için `sccache` ve `protobufer` neymiş araştırın.

```
cargo install sccache
```
```
sudo apt-get install protobuf-compiler
```

## `fleek-network/ursa.git` 'i klonluyoruz.

* `make install` uzun sürecek.
* daha sonra version kontrol edin: `ursa --version`
* version: `ursa 0.1.0`

```
cd $HOME 
git clone https://github.com/fleek-network/ursa.git
cd ursa
```
```
make install
```
## ursa adlı bir screen'de node'u çalıştıralım:

* Loglar akıyorsa sorun yok.
* Loglar aktıktan sonra CTRL + A + D ile çıkın.

```
screen -S ursa
```
```
cd $HOME
cd ursa 
ursa
```

## altta ki dosyayı indiriyoruz ve kontrol ediyoruz:

```
curl https://ipfs.io/ipfs/bafybeidqdywrzg7c3b4dmm332m4b7uiakgitplz2pep2zntederxpj3odi -o basic.car
```
```
ursa rpc put basic.car
```
```
ursa rpc get bafybeifyjj2bjhtxmp235vlfeeiy7sz6rzyx3lervfk3ap2nyn4rggqgei ./output
```
```
ls -hl ./output
```

![image](https://user-images.githubusercontent.com/101149671/209468216-0aa9927c-c28f-4f0d-9423-2cde745a4f63.png)

## Kolay gelsin.
