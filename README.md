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
```
```
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
Kurulum tamamlandıktan sonra işlemler başarıyla gerçekleştiyse aşağıdaki gibi bir ekran çıktısı görmemiz gerekli.

![This is an image](https://i.imgur.com/G40jlCs.png)

Son olarak ctrl+a+d  tuş kombinasyonu ile screen ekranından çıkıyoruz.

Daha sonra kişisel bilgisayarımızdan windows komut satırını yönetici olarak çalıştıryoruz.

![This is an image](https://i.imgur.com/a5nbpb2.png)

Aşağıdaki komutta sunucuip yazan kısmı espresso node kurmuş olduğumuz sunucumuzun ip adresi ile değiştirip komut satırında çalıştırıyoruz.

```
netsh interface portproxy add v4tov4 listenaddress=127.0.0.1 listenport=80 connectaddress=sunucuip connectport=80
```

Aynı şekilde aşağıdaki komutta sunucuip yazan kısmı espresso node kurmuş olduğumuz sunucumuzun ip adresi ile değiştirip komut satırında çalıştırıyoruz.

```
netsh interface portproxy add v4tov4 listenaddress=127.0.0.1 listenport=60000 connectaddress=sunucuip connectport=60000
```
Artık CAPE cüzdan oluşturabiliriz. CAPE cüzdan oluşturmak için kişisel bilgisayarımızda bir tarayıcı açarak (örneğin chrome) adres satırına localhost yazıyor ve enter tuşuna basıyoruz.
