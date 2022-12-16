# AI-VisioSoft
Bu çalışma bilgi tabelası(Information plate) ve alışveriş tabelası(shop sign) olmak üzere iki tabela türünü ayırt eden bir nesne tespit algoritması oluşturmaktadır.

# Kullanılan Araçlar(Tool)
Çalışmada pytorch v1.13 ile YOLO v5 hızlı ve yüksek doğruluklu sonuç verdiği için kullanılmıştır. Geliştirme ortamı olarak sağladığı güçlü GPU'dan dolayı Google Colabratory kullanılmıştır.

# Veri Seti
2048x3000 piksel boyutunda 484 fotoğraftan oluşan veri seti eğitim döngülerinin süresini kısaltmak amacıyla 640x640 boyutlarına düşürülmüştür. Fotoğraflar %70 train %15 test ve %15 validation olmak üzere 3'e ayrılmıştır. json formatındaki annotation dosyası YOLO v5 için uygun olan .txt formatına çevirilmiştir. 

# Nasıl Çalıştırılır
Dosyaları indirdikten sonra 'dataset/data.yaml' dosyası içindeki dosya yolları düzenlenmelidir. Daha sonra 'main.ipynb' dosyası içindeki dosya yollarıda düzenlenip çalıştırılabilir.

NOT : 'main.ipynb' dosyasının çıktıları çok uzun olduğu için kodu incelemeyi zorlaştıracaktır. Bu sebeple çıktıları içermeyen sadece kodların bulunduğu 'main(not_include_outputs).ipynb' dosyası eklenmiştir.

# Eğitim ve Test
'main.ipynb' dosyası içinde hem eğitim hem de test işlemini yapacak kodlar yer almaktadır. Eğitim aşamasını yapmadan kaydedilmiş ağırlıklarla test işlemi yapmak için 'Step 1: Install Requirements' başlığı altındaki hücre ve daha sonra 'Testing With Trained Weights' başlığı altındaki hücrenin çalıştırılması yeterlidir.

# Parametre Optimizasyonu
Algoritmanın başarısını arttırmak için 30 farklı parametre 500 döngü(epoch) ile çaprazlama(crossover) yöntemi kullanılarak optimize edilmiştir. Optimize edilmiş hiperparametreler 'result/evolve_results/hyp_evolve.yaml' dosyasına kaydedilmiştir. Bu parametrelerin bazıları şunlardır:

* lro

* lr1

* Momentum

* Weight-decay

* iou_t

* perspective


# Sonuçlar
Elde edilen tüm sonuçlar 'results' dosyası içindedir. Eğitim aşamasında alınan sonuçlar ve döngü kayıtları 'training_results' dosyası içerisindedir. Test sonuçları 'predictions' dosyası içindedir.

NOT: Test veri kümesindeki tüm fotoğrafların(73 fotoğraf) tahmin sonuçları 'result/predictions' dosyasında yer almaktadır.

# Yazar
* Senar Ali YAMAÇ

