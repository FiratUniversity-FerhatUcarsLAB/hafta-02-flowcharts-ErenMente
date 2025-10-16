Ad Soyad: Muhammet Eren Mente
okul no: 250542026

Görev 3: Hastane Randevu ve Test Sistemi Pseudocode'u
1-)"Lütfen TC Kimlik Numaranızı giriniz."

2-)*TC Kimlik No doğrulandı mı? Evet ise git 3, Hayır ise "Hatalı giriş." git 1.*

3-)"Hoş geldiniz. Lütfen yapmak istediğiniz işlemi seçin: 1-Randevu Al, 2-Test Sonuçlarını Görüntüle"

4-)*Eğer seçim == 1 git 5, Eğer seçim == 2 git 13, değilse "Geçersiz seçim." git 3.*

5-)"Poliklinik seçiniz: 1-Dahiliye, 2-KBB, 3-Göz"

6-)*Seçilen polikliniğe ait doktorları listele.* "Doktor seçiniz veya poliklinik seçimine dönmek için 9'a basınız."

7-)*Eğer seçim == 9 git 5, değilse git 8.*

8-)*Seçilen doktora ait müsait randevu saatlerini listele.* "Saat seçiniz veya doktor seçimine dönmek için 9'a basınız."

9-)*Eğer seçim == 9 git 6, değilse git 10.*

10-)"Randevu Bilgileri: ... Onaylıyor musunuz?" *Evet ise git 11, Hayır ise git 5.*

11-)*Randevuyu kaydet.*

12-)"Randevunuz oluşturulmuştur. SMS ile bilgi gönderilecektir." *git 19.*

13-)*Hastaya ait test sonuçlarını kontrol et.*

14-)*Eğer **test_hazir_mi** == Hayır ise "Testiniz laboratuvarda işlem aşamasındadır." git 19.*

15-)*Eğer **sonuc_onayli_mi** == Hayır ise "Sonuçlarınız doktor onayı beklemektedir." git 19.*

16-)*Test sonuçlarını ekrana yazdır.*

17-)"Sonuçları PDF olarak indirmek ister misiniz?" *Evet ise git 18, Hayır ise git 19.*

18-)*"Sonuçlar PDF olarak indiriliyor..."*

19-)"Başka bir işlem yapmak ister misiniz?" *Evet ise git 3, Hayır ise git 20.*

20-)"Oturum kapatıldı. Sağlıklı günler dileriz." *git 1.*
