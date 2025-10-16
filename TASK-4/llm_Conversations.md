Muhammet Eren Mente
250542026

bu görevide aynı şekilde pseudocode'unu oluştur

Görev 4: Üniversite Ders Kayıt Sistemi

Sistem Açıklaması

Öğrenci ders kayıt sisteminin tüm kontrollerini ve kurallarını modelleyin.

Sistem Gereksinimleri:

Öğrenci girişi (öğrenci kimliği + şifre)

Ders listesini görüntüle (dönem)

Her ders için:

Kota kontrolü (zorunluluk)

Ön koşul dersi kontrolü (zorunluluk)

Zaman çakışması kontrolü (zorunluluk)

Kredi limiti kontrolü (toplam ≤ 35) (zorunluluk)

Ders ekle/bırak (dönem)

Danışman onayı gerekli mi? (GNO ¡ 2.5) (zorunluluk)

Kayıt özeti görüntüleme ve kayıt onayı

Elbette, anlaşıldı. Önceki görevlerin formatına ve mantığına uygun olarak, Üniversite Ders Kayıt Sistemi için istenen tüm gereksinimleri karşılayan pseudocode'u aşağıda hazırladım.

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
bunu dot diline de çevir

Elbette, üniversite ders kayıt sisteminin bu detaylı pseudocode'unu, Graphviz'de görselleştirebileceğin DOT diline çevirdim.

Bu şema, bir ders ekleme sürecindeki tüm ardışık kontrol kapılarını (kota, ön koşul, çakışma, kredi) ve ders bırakma ile kaydı tamamlama gibi farklı modüllere nasıl dallandığını net bir şekilde gösterir.

Aşağıdaki kodun tamamını kopyalayıp Graphviz Online gibi bir siteye yapıştırarak akış şemanızı oluşturabilirsiniz.

DOT Dili Kodu
Kod snippet'i
digraph Course_Registration_Flowchart {
    // Grafik ayarları
    rankdir=TB;
    node [shape=box, style="rounded,filled", fillcolor=lightblue, fontname="Arial"];
    edge [fontname="Arial"];

    // --- Giriş ve Başlangıç ---
    Login [label="1. Öğrenci No ve Şifre Gir", shape=ellipse, style=filled, fillcolor=khaki];
    CheckLogin [label="2. Giriş Başarılı mı?", shape=diamond, style=filled, fillcolor=lightyellow];
    Initialize [label="3. Seçilen Dersleri ve Krediyi Sıfırla"];
    
    // --- Ana Menü ---
    MainMenu [label="4. Ders Listesini ve Seçilenleri Göster", style=filled, fillcolor=beige];
    ActionChoice [label="5. İşlem Seç\n1-Ekle | 2-Bırak | 3-Tamamla", shape=diamond, style=filled, fillcolor=lightyellow];

    // --- Ders Ekleme Modülü ---
    subgraph cluster_AddCourse {
        label = "Ders Ekleme Modülü";
        style=filled;
        color=lightgrey;
        node [fillcolor=azure];

        EnterCourseCode [label="7. Eklenecek Ders Kodunu Gir"];
        CheckQuota [label="8. Kota Kontrolü", shape=diamond];
        CheckPrerequisite [label="11. Ön Koşul Kontrolü", shape=diamond];
        CheckConflict [label="13. Zaman Çakışması Kontrolü", shape=diamond];
        CheckCreditLimit [label="15. Kredi Limiti Kontrolü (<=35)", shape=diamond];
        AddCourse [label="16. Dersi Listeye Ekle"];
        UpdateCredit [label="17. Toplam Krediyi Güncelle"];
        AddSuccessMsg [label="18. Ders Başarıyla Eklendi"];
        
        // Hata Mesajları
        QuotaFail [label="Kota Dolu", shape=box, style=filled, fillcolor=moccasin];
        PrereqFail [label="Ön Koşul Sağlanmadı", shape=box, style=filled, fillcolor=moccasin];
        ConflictFail [label="Ders Saatleri Çakışıyor", shape=box, style=filled, fillcolor=moccasin];
        CreditFail [label="Kredi Limiti Aşıldı", shape=box, style=filled, fillcolor=moccasin];
    }

    // --- Ders Bırakma Modülü ---
    subgraph cluster_DropCourse {
        label = "Ders Bırakma Modülü";
        style=filled;
        color=lightgrey;
        node [fillcolor=honeydew];
        
        ShowSelectedCourses [label="20. Seçilen Dersleri Göster"];
        EnterDropCode [label="21. Bırakılacak Dersi Gir"];
        DropCourse [label="22. Dersi Listeden Çıkar, Krediyi Güncelle"];
        DropSuccessMsg [label="23. Ders Bırakıldı"];
    }

    // --- Kayıt Tamamlama Modülü ---
    CheckGPA [label="24. GNO Kontrolü", shape=diamond, style=filled, fillcolor=lightgoldenrodyellow];
    NeedsAdvisorApproval [label="26. Danışman Onayına Gönderildi", shape=box, style=filled, fillcolor=orange];
    RegistrationComplete [label="27. Kayıt Başarıyla Tamamlandı", shape=box, style=filled, fillcolor=lightgreen];
    ShowSummary [label="28. Kayıt Özetini Göster"];
    Logout [label="29. Oturum Kapatıldı", shape=ellipse, style=filled, fillcolor=khaki];

    // --- Akış Okları ---
    // Giriş ve Menü
    Login -> CheckLogin;
    CheckLogin:s -> Initialize [label="Evet"];
    CheckLogin:w -> Login:w [label="Hayır"];
    Initialize -> MainMenu;
    MainMenu -> ActionChoice;
    ActionChoice -> EnterCourseCode [label="1-Ekle"];
    ActionChoice -> ShowSelectedCourses [label="2-Bırak"];
    ActionChoice -> CheckGPA [label="3-Tamamla"];

    // Ders Ekleme Akışı (Başarılı Yol)
    EnterCourseCode -> CheckQuota;
    CheckQuota -> CheckPrerequisite [label="Kota Var", color=green];
    CheckPrerequisite -> CheckConflict [label="Ön Koşul Tamam", color=green];
    CheckConflict -> CheckCreditLimit [label="Çakışma Yok", color=green];
    CheckCreditLimit -> AddCourse [label="Limit OK", color=green];
    AddCourse -> UpdateCredit -> AddSuccessMsg -> MainMenu;

    // Ders Ekleme Akışı (Hatalı Yollar)
    CheckQuota -> QuotaFail [label="Kota Dolu", color=red];
    QuotaFail -> MainMenu;
    CheckPrerequisite -> PrereqFail [label="Ön Koşul Eksik", color=red];
    PrereqFail -> MainMenu;
    CheckConflict -> ConflictFail [label="Çakışma Var", color=red];
    ConflictFail -> MainMenu;
    CheckCreditLimit -> CreditFail [label="Limit Aşıldı", color=red];
    CreditFail -> MainMenu;

    // Ders Bırakma Akışı
    ShowSelectedCourses -> EnterDropCode -> DropCourse -> DropSuccessMsg -> MainMenu;
    
    // Kayıt Tamamlama Akışı
    CheckGPA -> NeedsAdvisorApproval [label="GNO < 2.5"];
    CheckGPA -> RegistrationComplete [label="GNO >= 2.5"];
    NeedsAdvisorApproval -> ShowSummary;
    RegistrationComplete -> ShowSummary;
    ShowSummary -> Logout;
    Logout -> Login [label="Yeni Oturum"];
}
bu ödevin algoritmasını açıkla maks 4 satır ile

Elbette, işte üniversite ders kayıt sisteminin algoritma mantığının en fazla 4 satırlık özeti:

Sistem, başarılı öğrenci girişiyle başlar ve öğrenciye ders ekleme, bırakma veya kaydı tamamlama seçenekleri sunan ana bir menüye yönlendirir. Ders ekleme işlemi; kota, ön koşul, zaman çakışması ve 35 kredi limiti gibi bir dizi zorunlu ve sıralı kontrol kapısından oluşur; herhangi bir kontrolde başarısız olunursa işlem iptal edilir. Kaydı tamamlama aşamasında ise öğrencinin not ortalaması (GNO) kontrol edilir; 2.5'ten düşükse kayıt danışman onayına sunulur, aksi halde anında tamamlanır. Tüm bu işlemler, öğrenci kaydı onaylayana kadar ana menüye dönen bir döngü içinde gerçekleşir ve kayıt onayıyla oturum sonlandırılır.
