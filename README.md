# LogAnalysis

Soru: Elimizde bir access.log dosyası var. Bu log dosyasından "GET /favicon.ico" requesti atan unique IP Adreslerini ayıklamak için gerekli bashscript? 

Cevap: cat access.log | grep "GET /favicon.ico" | awk '{print $1}' | sort -u

Komut Açıklaması:

1- cat komutu ile access.log dosyasını görüntüledim.
2- Görüntülenen bu dosyayı grep komutuna verdim, bu şekilde sadece  "GET /favicon.ico" requestini içeren satırları aldım.
3- Daha sonra grep çıktısını awk komutuna verdim, böylece satırların sadece ilk kolonunu yani IP adreslerini aldım.
4- Son olarak tekrar eden IP adreslerini kaldırarak sıralama yapması için awk çıktısını sort komutuna verdim.

 Bu şekilde access.log dosyasından  "GET /favicon.ico" requesti atan unique IP adreslerini almış oldum.

