# pingpongbuild

> Selamlar, bugün herhangi bir sunucu satın almadan mevcut sunucularımızın yanında bize eşlik edecek bir node'u kuracağız.

> Burada Linux üzerinden anlatacağım, ne yazık ki rivalz sunucularımıza kurmak için çok çabaladım lakin küçük sunucularda `Hyper-V` donanımı eksik.

> Elbette bu sunucuya sahip ve Rivalz çalıtıran birisi deneyebilir, farklı çözümler yaratıp bayramdan sonra buraya ekleyeceğim.

> Donanımsal problem yok, tıpkı [rivalz](https://github.com/ruesandora/Rivalz) gibi, [nodepay](https://github.com/ruesandora/Rivalz/blob/main/nodepay.md) gibi canımız istediğinde istediğimiz sunucularda çalıştırabiliriz.

> Duyurular ve güncellemeler için tweet atmıyorum, sadece [buradan](https://t.me/RuesAnnouncement) paylaşıyorum.

# Kurulum.

> Öncelikle kendimize [buradan](https://app.pingpong.build/points?invite_code=e6ny5YsT) bir Pingpong hesap oluşturuyoruz.

> Burası app ksımı ve app'de ki testnet işlemlerini de yapabilirsiniz - bu konuda chatte yardımlaşırsınız.

> Bu sayfada bazı işlemler yaptıktan sonra sağ üstte ki `MORE` kısmından `DePın Harvester` kısmına girelim.

> Hesabımızı oluşturduktan sonra `Devices` kısmından `Add` diyelim.

#

> Sunucumuza geçelim:

> Linux dağıtımı Ubuntu veya Debian olabilir.

```console

# pingpongu yüklüyoruz
wget https://pingpong-build.s3.ap-southeast-1.amazonaws.com/linux/latest/PINGPONG
```

#

```console
# docker kurulumu
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

# enter diyelim
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

sudo apt-get update

# y diyelim.
sudo apt-get install docker-ce

# kodları tek tek girelim.
sudo systemctl start docker
sudo systemctl enable docker

sudo usermod -aG docker $USER

docker run hello-world
```

```console
# başlatma
screen -S pin
```
#

> Bu komutu girmeden Add kısmına girdiğimizde en üstte bir key var <> silip komutun sonuna yerleştiriyoruz.

> Dashboardan Linux seçip Usage Priority seçeneğini seçelim.

```console
chmod +x ./PINGPONG && ./PINGPONG --key <KEY>
```

> screen içersinde komutu girelim.

> Dashboarddan da Let's Gooo! diyoruz ve aşağıdaki gibi bir çıktı.


<img width="370" alt="Ekran Resmi 2024-06-16 09 35 30" src="https://github.com/ruesandora/pingpongbuild/assets/101149671/5da1b540-1e67-4534-8059-0a30a49f646f">

> Çok çabaladım windows için ama gece ve bayram arifesi olduğu için ve donanımsal bir problem olduğu için mecbur linux anlattım.

> çözersem veya çözersek bu repoda birleştiririz.

> Bu node'u artık tüm linux sunucularınızda maliyetsiz bir şekilde çalıştırabilirsiniz.

> [Tokenomics](https://pingpong.discourse.group/t/pingpong-tokenomics-design-proposal-v0-1-0/21)
