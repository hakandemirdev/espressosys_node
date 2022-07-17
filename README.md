# espressosys testnet node kurulumu

işletim sistemi için gerekli güncellemeleri yapıyoruz.
```
sudo apt-get update  && sudo apt-get upgrade
```
Docker yazılımını indiriyor ve kuruyoruz.
```
sudo apt install docker
```
```
apt install docker.io
```
Curl kuruyoruz.
```
apt install curl
```
Docker compose dosyasını indiriyoruz.
```
curl https://www.espressosys.com/cape/docker-compose.yaml --output docker-compose.yaml
```
Docker compose kurulumu yapıyoruz.
```
apt install docker-compose
docker-compose pull
```
Screen kurulumu yapıyoruz.
```
apt install screen
```
Bir screen oluşturuyoruz.
```
screen -S espresso
```
Son olarak docker compose 'u çalıştırıyoruz.
```
docker-compose up
```
