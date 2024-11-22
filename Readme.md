![image](https://github.com/user-attachments/assets/1a495447-e4a5-4f4f-9824-1feb0643c067)


# Glacier Node Kurulum : 

## Gereksinimler : 

Minimum : 

- 1 CPU+ / 2 GB RAM /  4 MBit/sec İndirme Hızı

Tavsiye Edilen : 

- 2+ CPU ( Hızlı ) / 4+ GB RAM / 8+ MBit/sec İndirme Hızı 

## Kayıt Ve Görevler : 

![image](https://github.com/user-attachments/assets/312b79b9-5e6f-4c9f-93a5-6fb63f491235)


- Kayıt : https://www.glacier.io/points/?inviter=0x44154Bc0a4d48B47b53DadCcF92923af9644E288

- Galxe Görevleri bulunuyor - görevleri yapmayı unutmayın - 3. kısımdan cüzdan bağlayıp arkadaşlarınızı davet edebilirsiniz.

## Testnet Tokenleri : 

- Testnet BNB Faucet: https://www.bnbchain.org/en/testnet-faucet

- Bridge : https://opbnb-testnet-bridge.bnbchain.org/deposit


Sistem paketlerini güncellemek ve yükseltmek için aşağıdaki komutu çalıştırın:

```bash
sudo apt update -y && sudo apt upgrade -y
```
## 2. Gerekli paketleri kurun:

```bash
sudo apt install htop ca-certificates zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev tmux iptables curl nvme-cli git wget make jq libleveldb-dev build-essential pkg-config ncdu tar clang bsdmainutils lsb-release libssl-dev libreadline-dev libffi-dev jq gcc screen unzip lz4 -y
```
## 3. Docker'ı Kur : 

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io -y
docker version
```

## 4. Docker Compose'u Kur : 

```bash
VER=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep tag_name | cut -d '"' -f 4)
curl -L "https://github.com/docker/compose/releases/download/$VER/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
docker-compose --version
```

## 4. Docker Kullanıcı İzinleri

```bash
sudo groupadd docker
sudo usermod -aG docker $USER
```

## Node'u Başlatalım : 

```bash
docker run -d -e PRIVATE_KEY=Metamask_Private_Keyin --name glacier-verifier docker.io/glaciernetwork/glacier-verifier:v0.0.1
```

## Loglar - Son 150 LOG : 

```bash
docker logs -f glacier-verifier -n 150
```

## Web Kontrol : 

- Link : https://testnet.nodes.glacier.io/status


