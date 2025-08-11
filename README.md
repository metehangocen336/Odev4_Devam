Bu proje, farklı büyük dil modelleri ,Gemma,Gpt5-nano,LLMA (LLM) ile yapılan etiketleme ve çıktı üretme denemelerinin kayıtlarını içeriyor.
Amaç, aynı veri setini farklı LLM’lere göndererek sonuçları karşılaştırmak, kullanılan promptları saklamak ve çıktıların doğruluğunu gözlemlemekti.

Genel Süreç
Her denemede konuşmaların tamamı doğrudan modele yollandı.

Modellerden gelen cevaplar, istenilen formatta olmasa bile kaydedildi.

Çıktılar hem JSON hem de ekran görüntüsü (PNG) olarak arşivlendi.

Kullanılan tüm promptlar, ilgili denemenin yanında .txt dosyası olarak tutuldu.

Doğruluk oranı net olarak ölçülmedi, ancak genel izlenime göre GPT-5 nano diğer denemelere kıyasla en iyi sonuçları verdi.

Klasör Yapısı ve İçerikler
llmoutputs/denemeler/
Bu klasör, yapılan tüm LLM denemelerinin kayıtlarını içerir.
Her model için şu dosyalar bulunur:

*.json → Modelden gelen ham çıktı.

prompt.txt → Denemede kullanılan prompt.

output.png → Model cevabının ekran görüntüsü (başarısız veya eksik olsa bile).

Her model birden fazla kez test edildi, dolayısıyla aynı model için birden çok alt klasör olabilir.

kontrol/
Bu klasör, LLM’e gönderilecek verilerin kontrol edildiği yer.

Buradaki dosyalar, modele gidecek içeriklerin son halini gösterir.

Amaç, yanlış veya eksik veri göndermemek için bir ara kontrol noktası oluşturmaktı.

Denemeler Hakkında Notlar
Farklı LLM sürümleriyle çalışıldı (ör. GPT-5 nano, GPT-4, başka alternatif modeller).

Her model, aynı veri setiyle birden fazla kez çalıştırıldı.

Çıktıların tamamı mükemmel değil — bazıları eksik, bazıları format dışı.

Buna rağmen, bütün sonuçlar arşivlenerek ileride karşılaştırma yapılabilecek bir veri tabanı oluşturuldu.

Karşılaşılan Sorunlar
API Çağrısı Limitleri

Bazı denemelerde API sınırına ulaşıldı ve işlem tamamlanamadı.

İstenen Formatın Tutmaması

Modeller bazen verilen format talimatlarını dikkate almadı.

JSON içinde eksik alanlar veya yanlış etiketlemeler görüldü.

Eksik / Hatalı Etiketlemeler

Tüm veriler doğru şekilde etiketlenmedi.

Bazı durumlarda model, verinin bir kısmını işlemden geçirmedi.

Farklı Deneme Sonuçlarının Tutarsızlığı

Aynı model, aynı veri setinde farklı çıktılar verebildi.

Bunun sebebi modelin deterministik olmaması veya prompt değişiklikleri olabilir.

Sonuç
Bu proje, LLM’lerle yapılan çoklu denemelerin hem teknik hem de pratik açıdan kayıt altına alındığı bir çalışma.
Çıktılar mükemmel olmasa bile, elde edilen veri ve deneyimler ileride daha isabetli LLM testleri için yol gösterici olacak.
