# fish_classification_ANN_Deep-Learning
Bu proje, bir balık türü sınıflandırma modeli geliştirmeyi amaçlıyor. "A Large Scale Fish Dataset" kullanılarak ANN modeliyle  öğrenme uygulanıyor. Eğitim ve doğrulama verileri kullanılarak modelin performansı değerlendirilip, sınıflandırma raporu ve karışıklık matrisiyle sonuçlar analiz ediliyor.

Veri Seti: https://www.kaggle.com/datasets/crowww/a-large-scalefish-dataset/data

Projenin kaggle linki : https://www.kaggle.com/code/rukiyekaraatli/fish-ann/edit/run/202678227

data DataFrame'indeki ilk 9 görüntüyü ve etiketlerini 3x3'lük bir grid üzerinde gösterir. Görüntüler 224x224 boyutuna ayarlanıp normalize edildikten sonra, her birine ait etiket başlık olarak eklenir ve görseller eksensiz olarak ekranda gösterilir.

![image](https://github.com/user-attachments/assets/e331db9d-fdb4-44a6-927c-022586eaef86)

BİRİNCİ MODEL sonuçları:

Classification Report:
                    precision    recall  f1-score   support

   Black Sea Sprat       0.12      0.11      0.12       400
   Gilt-Head Bream       0.15      0.11      0.13       400
   Hourse Mackerel       0.11      0.11      0.11       400
        Red Mullet       0.08      0.09      0.08       400
     Red Sea Bream       0.11      0.15      0.13       400
          Sea Bass       0.14      0.11      0.12       400
            Shrimp       0.11      0.18      0.14       400
Striped Red Mullet       0.13      0.12      0.12       400
             Trout       0.13      0.07      0.09       400

          accuracy                           0.12      3600
         macro avg       0.12      0.12      0.11      3600
      weighted avg       0.12      0.12      0.11      3600

    
![image](https://github.com/user-attachments/assets/3abdd295-eeae-4597-b3ab-b494624a5259)

![image](https://github.com/user-attachments/assets/b6c697c2-bb1d-4175-a402-374a6acf272e)

SONUÇ: Modelin genel doğruluğu %75.7 olsa da, türler bazında performansı düşük. Precision, recall ve f1-skorları 0.11 ile 0.18 arasında değişiyor, bu da modelin tahminlerinin çoğu tür için yetersiz olduğunu gösteriyor. Genel doğruluk iyi görünse de, modelin tüm sınıflar arasında tutarlı bir performansı yok ve iyileştirmeye ihtiyaç var.

İKİNCİ MODEL sonuçları:

Classification Report:
                     precision    recall  f1-score   support

   Black Sea Sprat       0.11      0.10      0.10       400
   Gilt-Head Bream       0.13      0.16      0.14       400
   Hourse Mackerel       0.11      0.09      0.10       400
        Red Mullet       0.11      0.11      0.11       400
     Red Sea Bream       0.11      0.09      0.10       400
          Sea Bass       0.10      0.13      0.11       400
            Shrimp       0.10      0.11      0.10       400
Striped Red Mullet       0.13      0.12      0.13       400
             Trout       0.13      0.12      0.12       400

          accuracy                           0.11      3600
         macro avg       0.11      0.11      0.11      3600
      weighted avg       0.11      0.11      0.11      3600

![image](https://github.com/user-attachments/assets/6ff3e9b9-2c0f-4c43-970c-dc0db4e288f6)

![image](https://github.com/user-attachments/assets/6f28f21c-9e85-48fc-9e2c-4bd896d6a5d4)

SONUÇ: Bu sonuçlar, modelin doğrulama doğruluğunun %90.2'ye yükseldiğini gösteriyor, yani model genel olarak veri setini iyi tanımlıyor. Ancak, classification report'a göre tür bazında modelin performansı hala düşük. Precision, recall ve f1-skorları türler arasında %9 ile %16 arasında değişiyor. Bu da modelin bazı türleri doğru sınıflandırmakta zorlandığını, genel doğruluğun yüksek olmasına rağmen türler arasında dengesiz bir performans olduğunu gösteriyor. Model, belirli balık türleri üzerinde daha fazla iyileştirmeye ihtiyaç duyuyor.


