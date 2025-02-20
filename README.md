# Nexus Prover Node
Anda mendapatkan Poin NEX dengan berkontribusi komputasi dan berinteraksi dengan ekosistem Nexus.


---

## --> Contribute via CLI
### 1. Install Dependecies
```bash
sudo apt update & sudo apt upgrade -y
sudo apt install screen curl libssl-dev pkg-config build-essential git-all protobuf-compiler -y
sudo apt update
```
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
```bash
source $HOME/.cargo/env
```
```bash
rustup target add riscv32i-unknown-none-elf
```
```bash
rustup target add riscv32i-unknown-none-elf
```
```bash
cargo config --global set build.unstable-features true
```

### 2. Run Prover
**1- Start a screen to keep it running in the background**
```bash
screen -S nexus
```
**2- Install and run prover**
```bash
curl https://cli.nexus.xyz/ | sh
```

### 3. Link Node
1- After installation command completes, it asks you if you want to link your node press `2`
![image](https://github.com/user-attachments/assets/603d8a8e-5be5-485d-b4b8-76a9639aa836)

2- Enter you `node-id`
* To find your `node-id`, go  to https://app.nexus.xyz/nodes
* Click `Add Node`, click `Add CLI Node` and copy your `node-id` and paste in terminal

![image](https://github.com/user-attachments/assets/754e4b13-9400-4108-9c3f-b0bba6c40132)


### 4. Manage your Node screen:
* To minimze the screen: `CTRL+A+D`

* To return to screen: `screen -r nexus`

* To kill screen: `screen -XS nexus quit`

## 5. If your RAM is not enough you can add manual using swap
```bash
sudo fallocate -l 24G /swapfile &&
sudo chmod 600 /swapfile &&
sudo mkswap /swapfile &&
sudo swapon /swapfile &&
sudo cp /etc/fstab /etc/fstab.bak &&
echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab

```
Edit 24G with your VPS RAM example if your VPS RAM is 6 GB change to 6 GB

---


