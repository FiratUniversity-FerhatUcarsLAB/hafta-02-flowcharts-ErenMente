Muhammet Eren Mente
250542026

1-)*Sistem_aktif_mi? Evet ise git 2, Hayır ise bekle ve git 1.*

2-)*Sensörleri oku (sürekli döngü).*

3-)*Eğer **hareket_algilandi** == Evet VEYA **kapi_pencere_acik** == Evet git 4, değilse git 2.*

4-)*Kameraları aktive et ve kayıt başlat.*

5-)*Ev sahibinin konumu kontrol et.*

6-)*Eğer **ev_sahibi_evde_mi** == Evet git 7, değilse git 8.*

7-)"Yanlış alarm. Sistem normal moda dönüyor." *git 2.*

8-)*Alarm seviyesini ayarla (1-Düşük, 2-Orta, 3-Yüksek).*

9-)*Belirlenen seviyeye göre bildirimleri gönder (SMS, Uygulama, E-posta).*

10-)*30 saniye bekle.*

11-)*Sensörleri tekrar kontrol et.*

12-)*Eğer **tehdit_devam_ediyor_mu** == Hayır git 13, değilse git 14.*

13-)"Tehdit ortadan kalktı. Alarm sıfırlanıyor." *git 2.*

14-)*Alarmı devam ettir (Siren çal, yetkililere haber ver).*

15-)*Kullanıcıdan sistemi devre dışı bırakma komutu bekle.*

16-)*Eğer **devre_disi_birak_komutu** == Evet git 17, değilse git 15.*

17-)"Sistem kullanıcı tarafından devre dışı bırakıldı. Normal moda dönülüyor." *git 2.*
