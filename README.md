# Quai Node Wrangler Rolü için Kurulum Adımları...

![Banner Resmi](https://i.hizliresim.com/1ki58xs.png)

## Minimum Sistem Gereksinimler

### İron Age Test Ağı sırasında Global bir düğüm çalıştırmak için aşağıdaki özelliklere sahip bir MacOS veya Ubuntu Vps ihtiyacınız olacak:

* 8+ çekirdekli vCPU
- 32 GB+ RAM
+ En az 3 TB boş alana sahip hızlı SSD
* 10+ MBit/sn indirme İnternet hizmeti
  
### İron Age Testağı sırasında bir Slience düğümü çalıştırmak için aşağıdaki özelliklere sahip bir MacOS veya Ubuntu Vps ihtiyacınız olacak:

* 4+ çekirdekli vCPU
* 16 GB RAM
* 1 TB SSD
* 10+ MBit/sn indirme İnternet hizmeti

> Yukarıdaki donanım özellikleri, Quai Network'ün yüksüz/düşük yükte çalıştığı zamanlar içindir. Quai Network yüksek/maksimum yükte çalışırken gerekli donanım özelliklerine ihtiyacınız olabilir.

## Bağımlılıkları Yükle

### Ubuntu
>
> `sudo apt install snapd` </br>
> `sudo snap install go --classic`
>
### MacOs
> `brew install go`

## Git & Make

### Ubuntu 
> `sudo apt install git make` </br>

### MacOs
> `brew install git make` 

## Install go-quai
> `git clone https://github.com/dominant-strategies/go-quai`  </br>
> `cd go-quai`  </br>
> `git fetch --all`

## .Env Düzenleme

> `cp network.env.dist network.env` </br>
> `nano network.env`

> Sistemi Düşük Olan Slience Node Çalıştırmak isteyen Aşağıdaki gibi istediği bölgeyi seçip onu yazsın. </br>
> Cyprus-1	[0 0]	</br>
> Cyprus-2	[0 1]	</br>
> Cyprus-3	[0 2]	</br>
> Paxos-1	[1 0]	</br>
> Paxos-2	[1 1]	</br>
> Paxos-3	[1 2]	</br>
> Hydra-1	[2 0]	</br>
> Hydra-2	[2 1]	</br>
> Hydra-3	[2 2] </br>

![Banner Resmi](https://i.hizliresim.com/krevh4a.jpg) 

![Banner Resmi](https://i.hizliresim.com/bq7m2zz.jpg)
![Banner Resmi](https://i.hizliresim.com/avrjqmk.jpg)

### CTRL + X -> Y -> Enter

## Nodumuzu Başlatıyoruz

> `make go-quai` </br>
> `make run`

## Log'ları Kontrol Ediyoruz

# Zone Kısmına Slience bölgesi hangisini seçtiyseniz onla değiştirin. Örnek zone-0-1.log,zone-2-2.log,zone-2-1.log gibi...
> `tail -f nodelogs/zone-0-0.log`

### CTRL + C Çıkış yapıyoruz.

## Sync Kontrol

> `tail -f nodelogs/* | grep Appended` </br>

## Böyle Akıyorsa Sorunsuz Çalışıyordur.Tebrikler...
![Banner Resmi](https://i.hizliresim.com/cw1jegq.jpg)

https://stats.quai.network/ Adresinden Kullanıcı Adımızı Kontrol Ediyoruz...





