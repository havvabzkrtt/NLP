 # 📌 Diller / Languages
- 🇹🇷 [Türkçe için tıklayın](#türkçe)
- 🇬🇧 [English version](#english)

# GB English

# 🛍️ Sentiment Analysis on Amazon Kozmos Reviews (NLP Application)

This project was developed with the goal of analyzing customer reviews of Kozmos products on Amazon to support product improvement and boost sales.

---

## 1. Project Objectives

Kozmos is a manufacturer focused on home, textile, and daily wear products.  
The aim of this project is to label customer reviews on Amazon using sentiment analysis, and to classify them into positive and negative categories using **Logistic Regression** and **Random Forest Regression** models.

---

## 2. Dataset

The dataset is provided in CSV format with the following columns:

- `"Star"`: Number of stars (rating)
- `"Helpful"`: Number of users who found the review helpful
- `"Title"`: Title of the review
- `"Review"`: Review text

---

## 3. Text Preprocessing

The following preprocessing steps were applied to the reviews:

- All words were converted to lowercase.
- Punctuation marks were removed and replaced with spaces.
- Numerical expressions were removed.
- Common stopwords were eliminated.
- Word frequencies were calculated and low-frequency words were removed.
- Lemmatization was applied to each word.

---

## 4. Text Visualization

- A **bar plot** was used to visualize word frequencies.
- A **WordCloud** was generated based on word frequency to represent keywords visually.

---

## 5. Sentiment Analysis

Using `SentimentIntensityAnalyzer`, each review was labeled as:
- **pos** (positive),
- **neg** (negative), or
- **neutral**.

---

## 6. Preparation for Modeling

- The `sentiment_label` column was converted to binary (1 for positive, 0 for negative).
- The dataset was split into training and testing sets.
- Text representations were converted into numerical form.
- A **Random Forest Classifier** model was trained.

---

## 7. Random Forest Regression Modeling

Random Forest is a popular algorithm for both classification and regression problems.  
Cross-validation of the model yielded a **98% accuracy score**.

---

## 8. Model Comparison Table

| Model                    | Accuracy Rate |
|--------------------------|---------------|
| Logistic Regression      | 97%           |
| Random Forest Regression | 98%           |




# 🇹🇷 Türkçe

# Amazon Kozmos Yorumları İçin Duygu Analizi (NLP Uygulaması)

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

