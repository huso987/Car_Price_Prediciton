# Araba Fiyat Tahmin Modeli

Bu proje, farklı araba özelliklerine dayanarak araba fiyatlarını tahmin etmek için bir makine öğrenimi modeli geliştirmeyi amaçlamaktadır. Proje, veri ön işleme, model eğitimi ve değerlendirmesi ile kullanıcıdan alınan özelliklere göre fiyat tahmini yapmayı içerir.

## İçindekiler
- [Genel Bakış](#genel-bakış)
- [Veri Kümesi](#veri-kümesi)
- [Gereksinimler](#gereksinimler)
- [Kurulum](#kurulum)
- [Model Eğitimi](#model-eğitimi)
- [Fiyat Tahmini](#fiyat-tahmini)
- [Sonuçlar](#sonuçlar)
- [Katkıda Bulunanlar](#katkıda-bulunanlar)

## Genel Bakış
Bu proje, araba özelliklerine dayalı olarak fiyat tahmini yapmak için çeşitli makine öğrenimi algoritmalarını kullanır. Kullanılan veri kümesi, farklı araba özelliklerini ve fiyat bilgilerini içerir. Projede, Linear Regression ve Random Forest modelleri kullanılmış ve en iyi sonuç veren model Grid Search ile optimize edilmiştir.

## Veri Kümesi
Veri kümesi, araba özelliklerini ve fiyatlarını içeren bir CSV dosyasından oluşmaktadır. Veri kümesi, aşağıdaki sütunları içermektedir:

- car_ID
- symboling
- CarName
- fueltype
- aspiration
- doornumber
- carbody
- drivewheel
- enginelocation
- wheelbase
- carlength
- carwidth
- carheight
- curbweight
- enginetype
- cylindernumber
- enginesize
- fuelsystem
- boreratio
- stroke
- compressionratio
- horsepower
- peakrpm
- citympg
- highwaympg
- price

  ![image](https://github.com/user-attachments/assets/1dfec23e-d23b-40b2-b9ba-e20fe55de689)           ![image](https://github.com/user-attachments/assets/1f46da0f-5ef5-4063-ba0a-a4598a7731b1)


  ![image](https://github.com/user-attachments/assets/74e06994-a87c-42d2-90e5-8309cad068b7)

                                       


## Gereksinimler
Bu projeyi çalıştırmak için aşağıdaki Python kütüphanelerine ihtiyacınız olacak:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

Bu kütüphaneleri yüklemek için aşağıdaki komutu kullanabilirsiniz:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn

## Kurulum
Projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları izleyin:
1) git clone https://github.com/kullanici-adi/araba-fiyat-tahmin.git
2) cd araba-fiyat-tahmin
3) pip install -r requirements.txt

## Model Eğitimi
Proje, Linear Regression ve Random Forest algoritmaları ile model eğitimi yapmaktadır. Ayrıca, Grid Search kullanılarak Random Forest modelinin hiperparametreleri optimize edilmiştir.

Model Performansı
Linear Regression MSE: 19845915.05
Linear Regression R2: 0.74
Random Forest MSE: 10396950.27
Random Forest R2: 0.87
Best Random Forest MSE: 9623056.42
Best Random Forest R2: 0.88

## Fiyat Tahmini
Aşağıdaki örnek girdi verileri kullanılarak fiyat tahmini yapılmıştır:

                                                    example_input = {
                                                        'symboling': 3,
                                                        'fueltype': 'gas',
                                                        'aspiration': 'std',
                                                        'doornumber': 'four',
                                                        'carbody': 'sedan',
                                                        'drivewheel': 'fwd',
                                                        'enginelocation': 'front',
                                                        'wheelbase': 88.6,
                                                        'carlength': 168.8,
                                                        'carwidth': 64.1,
                                                        'carheight': 48.8,
                                                        'curbweight': 2548,
                                                        'enginetype': 'dohc',
                                                        'cylindernumber': 'four',
                                                        'enginesize': 130,
                                                        'fuelsystem': 'mpfi',
                                                        'boreratio': 3.47,
                                                        'stroke': 2.68,
                                                        'compressionratio': 9.0,
                                                        'horsepower': 111,
                                                        'peakrpm': 5000,
                                                        'citympg': 21,
                                                        'highwaympg': 27
                                                    }
                                                    
                                                    Tahmin edilen araba fiyatı: $13207.13
## Sonuçlar
![image](https://github.com/user-attachments/assets/326389f0-ef82-4575-a899-ce0a26d8553d)

## Katkıda Bulunanlar

Data seti https://www.kaggle.com/code/hellbuoy/carprice-prediction-mlr-rfe-vif/input   linkinden aldık


