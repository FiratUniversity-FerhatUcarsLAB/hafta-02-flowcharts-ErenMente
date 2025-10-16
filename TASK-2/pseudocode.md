Bu pseudo kod Google Gemini tarafından tasarlanmıştır.

1-)"Lütfen giriş yapınız."

2-)*Kullanıcı giriş yaptı mı? Evet ise git 4, Hayır ise git 1.*

3-)***sepet** = boş*

4-)"Kategoriler: 1-Elektronik, 2-Kitap. Seçim yapınız veya sepet için 0'a basınız."

5-)*Eğer seçim == 0 git 12, değilse git 6.*

6-)*Seçilen kategori ürünlerini listele.*

7-)"Sepete eklemek istediğiniz ürünü seçiniz veya üst menü için 9'a basınız."

8-)*Eğer seçim == 9 git 4, değilse git 9.*

9-)*Seçilen ürünün stoğunu kontrol et.*

10-)*Eğer **stok** > 0 git 11, değilse "Ürün stokta yok." git 4.*

11-)*Ürünü **sepet**'e ekle. "Ürün sepete eklendi." git 4.*

12-)***sepet**'i ve **sepet_toplami**'nı göster.*

13-)"1-Alışverişe Devam, 2-Ödemeye Geç"

14-)*Eğer seçim == 1 git 4, değilse git 15.*

15-)"İndirim kodunuz var mı?" *Evet ise git 16, Hayır ise git 19.*

16-)"Kodu giriniz."

17-)***indirim_kodu**'nu kontrol et.*

18-)*Eğer kod geçerli ise indirimi uygula ve **sepet_toplami**'nı güncelle, git 19. Değilse "Geçersiz kod." git 15.*

19-)*Eğer **sepet_toplami** < 50 git 20, değilse git 21.*

20-)"Minimum sepet tutarı 50 TL olmalıdır." *git 4.*

21-)***kargo_ucreti** = 20 TL*

22-)*Eğer **sepet_toplami** >= 200 ise **kargo_ucreti** = 0.*

23-)***genel_toplam** = **sepet_toplami** + **kargo_ucreti**.*

24-)"Toplam Tutarınız: " *+ **genel_toplam**.*

25-)"Ödeme Yöntemi Seçin: 1-Kredi Kartı, 2-Havale"

26-)"Siparişi onaylıyor musunuz?" *Evet ise git 27, Hayır ise git 12.*

27-)*Siparişi kaydet. Ürün stoklarını güncelle.*

28-)"Siparişiniz başarıyla alınmıştır. Teşekkür ederiz." *git 1.*
