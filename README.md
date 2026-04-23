# Endüstriyel Sıralı Valf Kontrol Sistemi (State Machine)

Bu proje, CODESYS ortamında **Structured Text (ST)** kullanılarak geliştirilmiş bir endüstriyel durum makinesi (State Machine) uygulamasıdır. 

## 🛠️ Kullanılan Teknolojiler
* **Yazılım:** CODESYS V3.5
* **Dil:** Structured Text (IEC 61131-3)
* **Arayüz:** CODESYS Visualization (HMI)

## ⚙️ Sistemin Çalışma Mantığı
Sistem, 3 adet valfin (pistonun) belirli zaman aralıklarıyla ardışık olarak kontrol edilmesini sağlar:
1. Makinenin devreye girmesi için operatörün **10 saniye içerisinde** 3 ayrı Start butonuna basması (bas-çek / R_TRIG) zorunludur. Basılı tutma durumunda sistem güvenliği devreye girer.
2. Şart sağlandığında valfler sırasıyla (2sn, 1sn, 1.5sn vb.) ileri ve geri hareketlerini yapar.
3. Döngü, operatör müdahalesi olana kadar devam eder.
4. **Güvenli Duruş (Stop):** Stop butonuna basıldığında sistem anında enerjiyi kesmez; valfleri 1, 2 ve 3 sırasıyla güvenli (Home) pozisyonuna çeker.





