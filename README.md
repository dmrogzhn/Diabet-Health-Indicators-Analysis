
# Diyabet Veri Seti Analizi ve Ön İşleme

Bu proje, bir diyabet veri setinin analizini ve ön işlemesini yaparak veri setini model eğitimi için uygun hale getirmeyi amaçlamaktadır. Veri seti, bireylerde diyabet ihtimalini gösterebilecek sayısal değişkenleri içermektedir.

## Proje Amaçları

1. **Veri Temizleme ve Ön İşleme**:
   - Eksik verilerin doldurulması.
   - Aykırı değerlerin tespiti ve işlenmesi.
   - Veri setini geliştirmek için özellik mühendisliği yapılması.

2. **Model Önerileri Sunmak**:
   - Veri seti üzerinde tahmin yapmak için uygun modellerin önerilmesi.

## Veri Seti Hakkında

- **Kaynak**: Veri seti [Kaggle](https://www.kaggle.com) platformundan edinilmiştir.
- **Özellikler**: Veri seti, BMI, yaş, kan basıncı, fiziksel aktivite göstergeleri gibi diyabet ihtimalini etkileyebilecek çeşitli sayısal özellikler içerir.
- **Hedef Değişken**: `Diabetes_binary` - Bireyin diyabet hastası olup olmadığını (1: Diyabet, 0: Sağlıklı) belirten ikili bir etiket.

## Veri Ön İşleme Süreci

1. **Eksik Verilerin Doldurulması**:
   - İkili (binary) sütunlar için **mod** değeri kullanıldı.
   - Sürekli sayısal sütunlar için, uç değerlerden etkilenmemesi adına **medyan** kullanıldı.
   - Sayısal sütunlar için normal dağılım kontrolü yapıldı.

2. **Aykırı Değerlerin Belirlenmesi ve İşlenmesi**:
   - Aykırı değerler **Çeyrekler Arası Aralık (IQR)** yöntemi ile tespit edildi.
   - Kabul edilebilir aralıkların dışındaki değerler, ilgili sütuna göre **mod** (binary sütunlar) veya **medyan** (sayısal sütunlar) ile değiştirildi.

3. **Özellik Mühendisliği**:
   - Farklı yaş grupları için ortalama BMI değerleri hesaplanarak bireyin yaşıtlarına göre durumunu gösteren bir özellik oluşturuldu.
   - WHO’nun BMI sınıflandırma kriterlerine göre bireyler (ör. normal, aşırı kilolu, obez) kategorilere ayrıldı.

## Görselleştirmeler

- **Boxplot**: Sayısal özelliklerin dağılımını ve aykırı değerleri analiz etmek için kullanıldı.
- **Histogram**: Sayısal verilerin dağılımını görselleştirmek için kullanıldı.
- **Eksik Veri Matrisi**: `missingno` kütüphanesi kullanılarak eksik veriler görselleştirildi.

## Kullanılan Araçlar ve Kütüphaneler

- **Python Kütüphaneleri**:
  - `pandas` - Veri manipülasyonu ve analizi.
  - `matplotlib` ve `seaborn` - Veri görselleştirme.
  - `missingno` - Eksik veri görselleştirme.
- **İstatistiksel Analiz**:
  - Normal dağılım kontrolleri ve çeyrek dilim hesaplamaları.

## Önerilen Sonraki Adımlar

- Bu temizlenmiş ve ön işlenmiş veri seti kullanılarak model eğitimi yapılabilir.
- Diyabet tahmini için uygun olabilecek bazı modeller:
  - Lojistik Regresyon
  - Random Forest
  - Gradient Boosting (ör. XGBoost, LightGBM)

## Teşekkür

Kaggle notebook adresim aşağıda verilmiştir
- Veri seti [Kaggle](https://www.kaggle.com/code/oguzhandemir/diabet-kernel) platformundan alınmıştır.

## İletişim
