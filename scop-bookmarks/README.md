# SCOP X kayıt klasörü arşivi

`@Tartismalar` hesabının **SCOP** X bookmark klasöründen dışa aktarılmış gönderi arşivi.

## Kaynak

| Alan | Değer |
| --- | --- |
| X hesap id | `1483914840750145546` (`Tartismalar`) |
| Klasör | SCOP (`1840521791996907615`) |
| Dışa aktarım (UTC) | 2026-11-06 07:16:06 UTC |
| Klasör API | `get_users_bookmarks_by_folder_id` |
| Gönderi API | built-in `x.get_posts_by_ids` (zengin alanlar + expansions) |

## Önemli sınırlama

Klasör endpoint’i **20 gönderi ID’si** döndürdü ve **`meta.next_token` yoktu** (`max_results=100` ile de aynı). Yani bu arşiv, API’nin o anda verdiği tam listeyi yansıtır; klasörde X arayüzünde daha fazla kayıt görünüyorsa API şu an sayfalamıyor / daha fazlasını vermiyor olabilir.

## Sayılar

- Klasörden gelen ID: **20**
- Tam okunan gönderi: **19**
- Erişilemeyen: **1** (yetki / private / silinmiş)

## Dosyalar

| Dosya | İçerik |
| --- | --- |
| `all-bookmarks.csv` | Tam metin, yazar, zaman, URL, tüm public metrics, medya URL’leri |
| `raw-posts.json` | `get_posts_by_ids` ham yanıtı (includes dahil) |
| `bookmark-ids.json` | Klasörden gelen 20 ID + meta notu |
| `unavailable.csv` | Okunamayan ID’ler ve neden |
| `scouting-overview.md` | Ham metinlerden çıkarılan isim/kulüp notları (uydurma yok) |
| `README.md` | Bu dosya |

## Erişilemeyen

- `2115858703131836671` — Authorization Error: Sorry, you are not authorized to see the post with ids: [2115858703131836671].

## Yeniden senkron

Aynı klasörden tekrar çekmek için (gh auth + X connector gerekir):

```bash
# 1) Klasör ID listesini al (user-X get_users_bookmarks_by_folder_id)
# 2) x get_posts_by_ids ile zengin alanlar
# 3) Bu dizindeki script / CSV üretim adımlarını tekrar çalıştır
```

Bu depoda rutin (cron) kurulmadı; ihtiyaç olunca manuel yeniden export yeter.
