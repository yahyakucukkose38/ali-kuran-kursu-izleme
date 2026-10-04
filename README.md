# Yaz Kur'an Kursu — canlı site izleme

Bu depo yalnızca [Yaz Kur'an Kursu uygulamasını](https://ali-kuran-kursu.ihyadijital.com) izler; kod ya da veri içermez.
GitHub Actions her 10 dakikada şunları denetler:

1. API ve veritabanı yanıt veriyor mu (`/api/v1/health`; anlık aksaklık için 30 sn arayla 3 deneme)
2. Giriş sayfası açılıyor mu
3. HTTPS sertifikasının bitmesine 14 günden fazla var mı

Bir adım başarısız olursa GitHub depo sahibine e-posta gönderir. Bildirimlerin açık olduğu yer:
GitHub → Settings → Notifications → **Actions** → “Send notifications for failed workflows only”, **Email** işaretli.

- **Elle denetim:** Actions → “Canlı site izleme” → Run workflow
- **Bildirim denemesi:** Aynı yerden “Bildirim e-postasının ulaştığını görmek için bilerek başarısız ol” işaretlenip çalıştırılır.
- **60 gün kuralı:** GitHub, herkese açık bir depoda 60 gün hiç değişiklik olmazsa zamanlanmış denetimi durdurur.
  Durdurmadan önce e-posta gönderir; Actions sayfasında “Enable workflow” ile yeniden açılır.

Yedekleme ve sunucu ayrıntıları ana projenin `deploy/README.md` dosyasındadır.
