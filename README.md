# yapay-zeka-proje-devi-
sağlık projesi: yan ekti örüntüsü eşleştirme
# Sağlık Projesi: İlaca Bağlı Yan Etki Örüntüsü Eşleştirme - Veri Ön İşleme

Bu notebook, openFDA Adverse Event veri setindeki yan etki açıklamalarını ön işleme tabi tutarak temizlenmiş bir corpus oluşturur. İşlemler:
- Küçük harfe çevirme
- Tokenizasyon (cümle ve kelime bazında)
- Stopword temizliği
- Lemmatizasyon ve Stemming
- Temizlenmiş veriyi CSV'ye kaydetme
- Kelime bulutu görselleştirme
- Açıklamalar
Veri Çekme: openFDA API’sinden 5.000 yan etki kaydı çektik. Her kayıt, bir yan etki açıklaması ve ilgili ilacı içeriyor.
Preprocessing: PDF’deki adımları aynen uyguladık:
Metni cümlelere ve kelimelere ayırdık.
Stopwords’leri kaldırdık.
Kelimeleri lemmatize ve stem ettik.
Çıktıları CSV’ye kaydettik.
Kelime Bulutu: Temizlenmiş veriyi görselleştirdik, hocanın 1. hafta raporlama talebine uygun olarak.
Hatalar: API bağlantısında hata alırsanız, internet bağlantınızı kontrol edin veya limit parametresini düşürün (örneğin, 1.000 kayıt).
Veri Boyutu ve Değişiklikler
Ham Veri: ~5.000 yan etki açıklaması, yaklaşık 10-20 MB (JSON formatında).
Temiz Veri: Stopwords kaldırıldı, kelimeler normalize edildi. Kelime sayısı yaklaşık %30-40 azaldı (stopwords ve gereksiz tokenlar çıkarıldı).
Raporlama: Kelime bulutu, temizlenmiş verideki en sık yan etkileri (örneğin, "nausea", "headache") öne çıkardı.
