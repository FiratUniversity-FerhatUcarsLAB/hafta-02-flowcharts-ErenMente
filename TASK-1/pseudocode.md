 *Bu pseudocode'un temel mantığı ve akış şeması tarafımdan oluşturulmuş, mantıksal hataların düzeltilmesi ve kritik adımların (bakiye güncellemesi vb.) eklenmesi sürecinde yapay zeka (Google Gemini) desteğinden faydalanılmıştır.*



![atm](https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExazZycGRrb3k0MXBwbnJibG5nOGRyYmI4Z2d3a2RtazNwOXk5MHlybSZlcD12MV9naWZzX3NlYXJjaCZjdD1n/Ifbl3BS14c725VUlpR/giphy.webp)

## Görev 1: ATM Para Çekme Sistemi

### Sistem Açıklaması
1-)*"Kartınızı giriniz."*

2-)Kart takılı mı? Evet ise git 3, Hayır ise git 1.

3-)**sayac** = 0

4-)*"Pin giriniz."*

5-)Pin doğru ise git 10, yanlış ise git 6.

6-)**sayac**++

7-)Eğer **sayac** < 3 git 8, değilse git 9.

8-)*"Yanlış pin, bir daha deneyin. Kalan hak: "* + (3-**sayac**) git 4.

9-)*"Kartınız bloke oldu geçmiş olsun bana da afiyet olsun.😋 =)"* git 25.

10-)Bakiyeyi sorgula git 11.

11-)"Çekmek istediğiniz tutarı giriniz."

12-)Eğer **istenen_tutar** > **bakiye** git 13, değilse git 14.

13-)"Yetersiz Bakiye." git 11.

14-)Eğer **istenen_tutar** % 20 == 0 git 16, değilse git 15.

15-)"Çekilmek istenen tutar 20'nin katı olmalıdır." git 11.

16-)Günlük limiti sorgula git 17.

17-)Eğer **istenen_tutar** > **günlük_limit** git 18, değilse git 19.

18-)"Günlük limiti aştınız." git 11.

19-)**bakiye** = **bakiye** - **istenen_tutar**

20-)**günlük_limit** = **günlük_limit** - **istenen_tutar**

21-)"Fiş ister misiniz?" Eğer evet ise git 22, değilse git 23.

22-)"Fişinizi alınız." git 23.

23-)"Paranızı alınız." git 24.

24-)"Başka işlem ister misiniz?" Evet ise git 3, değilse git 25.

25-)"İyi günler." git 1.


![splurge](https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExazZycGRrb3k0MXBwbnJibG5nOGRyYmI4Z2d3a2RtazNwOXk5MHlybSZlcD12MV9naWZzX3NlYXJjaCZjdD1n/1APhDggUPlkRdK5w1n/200.webp)
