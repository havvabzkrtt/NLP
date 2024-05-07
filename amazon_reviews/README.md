# Amazon Yorumları İçin Duygu Analizi (NLP Uygulaması)

Bu proje, Kozmos'un Amazon üzerindeki ürünlerine gelen yorumları analiz ederek, ürünlerin özelliklerini geliştirme ve satışlarını artırma hedefi doğrultusunda gerçekleştirilmiştir.

## 1. Proje Amaçları

Kozmos, ev, tekstil ve günlük giyim odaklı üretimler yapmaktadır. Bu projenin amacı, Amazon üzerindeki yorumları duygu analizi yaparak etiketlemek ve bu etiketlenmiş verilerle "Lojistik Regresyon" ve "Random Forest Regresyon" sınıflandırma modelleri oluşturarak pozitif ve negatif duyguları sınıflandırmaktır.

## 2. Veri Seti

Veri seti, CSV dosyasında yer almaktadır. Bu dosyadaki sütunlar şunlardır:

- "Star": Yıldız sayısı
- "Helpful": Yorumu kaç kişinin faydalı bulduğu
- "Title": Yorum başlığı
- "Review": Yapılan yorumlar

## 3. Metin Ön İşleme

Metin ön işleme aşamasında şu işlemler uygulanmıştır:

- Metindeki bütün kelimeler küçük harfe çevrilmiştir.
- Noktalama işaretleri kaldırılarak yerine boşluk eklenmiştir.
- Sayısal ifadeler çıkartılmıştır.
- Dilde yaygın kullanılan stopwords'ler temizlenmiştir.
- Kelimelerin frekansları hesaplanmış ve az geçen kelimeler çıkartılmıştır.
- Lemmatization işlemi uygulanmıştır.

## 4. Metin Görselleştirme

- Bartplot ile kelimelerin frekansları görselleştirilmiştir.
- WordCloud ile kelimelerin frekanslarına göre bir bulut şeklinde görsel oluşturulmuştur.

## 5. Duygu Analizi (Sentiment Modellemesi)

SentimentIntensityAnalyzer ile yorumlar etiketlenerek, "pos" (pozitif), "neg" (negatif) veya "nötr" anlamlarından hangisini taşıdığı tespit edilmiştir.

## 6. Modellemeye Hazırlık

- "sentiment_label" sütunundaki değerler 1 ve 0'a dönüştürülmüştür.
- Veri seti eğitim ve test olarak ayrılmıştır.
- Temsil şekilleri sayısala çevrilmiştir.
- RandomForestClassifier sınıfı kullanılarak bir model oluşturulmuştur.

## 7. Random Forest Regresyon Modelleme

Random forest, sınıflandırma ve regresyon problemleri için yaygın olarak kullanılan bir yöntemdir. Oluşturulan modelin çapraz doğrulaması yapılmış ve %98'lik bir başarı elde edilmiştir.

## 8. Karşılaştırma Tablosu

| Model                       | Başarı Oranı |
|-----------------------------|--------------|
| Lojistik Regresyon          | %97          |
| Random Forest Regresyon     | %98          |

