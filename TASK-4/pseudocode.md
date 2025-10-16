muhammet eren mente
250542026

Görev 4: Üniversite Ders Kayıt Sistemi Pseudocode'u
1-)"Öğrenci No ve Şifre giriniz."

2-)*Giriş başarılı mı? Evet ise git 3, Hayır ise "Hatalı giriş." git 1.*

3-)***secilen_dersler** = boş; **toplam_kredi** = 0*

4-)*Dönem derslerini ve güncel **secilen_dersler** listesini göster.*

5-)"İşlem seçin: 1-Ders Ekle, 2-Ders Bırak, 3-Kaydı Tamamla"

6-)*Eğer seçim == 1 git 7, Eğer seçim == 2 git 20, Eğer seçim == 3 git 24.*

7-)"Eklemek istediğiniz dersin kodunu giriniz."

8-)*Seçilen dersin kotasını kontrol et.*

9-)*Eğer **kota** > 0 git 10, değilse "Derste yer kalmamıştır." git 4.*

10-)*Öğrencinin aldığı dersleri kontrol et.*

11-)*Eğer **on_kosul_dersi** alınmış mı? Evet ise git 12, değilse "Ön koşul dersini almadınız." git 4.*

12-)*Seçilen dersin saatini **secilen_dersler**'in saatleriyle karşılaştır.*

13-)*Eğer **zaman_cakismasi** var mı? Hayır ise git 14, değilse "Ders saatleri çakışıyor." git 4.*

14-)*Yeni dersin kredisi ile **toplam_kredi**'yi topla.*

15-)*Eğer (yeni_kredi + **toplam_kredi**) <= 35 git 16, değilse "Kredi limitini (35) aşıyorsunuz." git 4.*

16-)*Dersi **secilen_dersler** listesine ekle.*

17-)***toplam_kredi** = **toplam_kredi** + yeni_kredi*

18-)"Ders başarıyla eklendi."

19-)*git 4*

20-)***secilen_dersler** listesini göster.*

21-)"Bırakmak istediğiniz dersin kodunu giriniz."

22-)*Dersi **secilen_dersler** listesinden çıkar ve **toplam_kredi**'yi güncelle.*

23-)"Ders bırakıldı." *git 4.*

24-)*Öğrencinin **GNO**'sunu kontrol et.*

25-)*Eğer **GNO** < 2.5 git 26, değilse git 27.*

26-)"GNO'nuz 2.5'ten düşük olduğu için kaydınız danışman onayına gönderilmiştir." *git 28.*

27-)"Ders kaydınız başarıyla tamamlanmıştır."

28-)*Kayıt özetini (**secilen_dersler** ve **toplam_kredi**) göster.*

29-)"Oturum kapatıldı." *git 1.*
