### Güncelleme
```console
cd
cd ~/fleek-network/lightning
git pull origin testnet-alpha-0

cargo +stable build --release
sudo rm -f "/usr/local/bin/lgtn"
sudo ln -s "~/fleek-network/lightning/target/release/lightning-node" /usr/local/bin/lgtn
systemctl restart lightning
sudo systemctl start lightning.service
```

### Watiliste başvurmanın kolay yolu
```console
curl -sS https://get.fleek.network/whitelist | bash
```
