# MAKİNE ÖĞRENİMİ ALGORİTMALARI İLE BEYİN TÜMÖRÜ TEŞHİSİ

## Giriş

Beyin tümörleri, çocuklarda ve yetişkinlerde görülen agresif hastalıklar arasında kabul
edilir. Merkezi Sinir Sistemi (MSS) tümörlerinin büyük çoğunluğunu oluştururlar ve tüm
MSS tümörlerinin %85-90'ını teşkil ederler

Literatürde yapılan çalışmalar, Makine Öğrenimi (ML) ve Yapay Zeka (AI) tekniklerinin
otomatik sınıflandırma için kullanılmasının, manuel sınıflandırmadan daha yüksek
doğruluk sağladığını ortaya koymuştur. Bu nedenle, Evrişimli Sinir Ağları (CNN), Yapay
Sinir Ağları (ANN) ve Makine Öğrenimi gibi Algoritmalar kullanılarak geliştirilen ve
beyin tümörlerinin tespit ve sınıflandırılmasında kullanılan sistemler, tıp uzmanlarına
büyük destek sağlayacaktır.

## Materyal ve Yöntem

### Geliştirme Ortamı

Bu proje, veri analizi, model geliştirme ve sonuçların görselleştirilmesi için Jupyter Lab
ortamında geliştirilmiştir. Jupyter Lab, interaktif veri bilimi ve makine öğrenimi projeleri
için güçlü bir araçtır ve kullanıcıların kod, veriler ve görsellerle etkileşimli olarak
çalışmasını sağlar. Projede Python programlama dili ve TensorFlow/Keras kütüphaneleri
kullanılarak beyin tümörü tespiti için derin öğrenme modeli geliştirilmiştir.

### Veri Seti

Toplamda 3060 adet beyin MRI görüntüsünden oluşan veri seti, Kaggle platformunda
bulunan "Br35H :: Brain Tumor Detection 2020" adlı bir veri setidir. Görüntüler, "yes"
(tumor), "no" (normal) ve "pred" olmak üzere üç farklı klasör altında düzenlenmiştir.
Tumor sınıfı 1500 görüntü içerirken, normal sınıfı da 1500 görüntüden oluşmaktadır.
"pred" klasöründe ise etiketsiz 60 görüntü bulunmaktadır. Bu çalışma kapsamında sadece
"yes" ve "no" klasörlerindeki toplam 3000 görüntü kullanılmıştır.

### Makine Öğrenimi Algoritmaları

Proje Decision Tree , KNN , Yapay Sinir Ağları ve Evrişimli Sinir ağları ile eğitilmiştir.

#### Decision Tree 
Karar ağacı, belirli bir soruna yönelik tüm potansiyel çözümleri haritalandıran akış şeması
benzeri bir diyagramdır. Genellikle kuruluşlar tarafından, bir dizi karar almanın tüm olası
sonuçlarını karşılaştırarak en uygun hareket tarzını belirlemeye yardımcı olmak için
kullanılır

#### KNN : K-NN algoritması, T. M. Cover ve P. E. Hart tarafından önerilen, örnek veri noktasının
bulunduğu sınıfın ve en yakın komşunun, k değerine göre belirlendiği bir sınıflandırma
yöntemidirK en yakın komşu (KNN) algoritması, adından da anlaşılacağı üzere,
komşularına bakarak tahminlemede bulunan bir algoritmadır. KNN algoritmasında,
benzer olan şeyler birbirine yakındır varsayımı geçerlidir.

#### Yapay Sinir Ağları : Sinir ağı, bilgisayarlara verileri insan beyninden esinlenerek işlemeyi öğreten bir yapay
zeka yöntemidir. Bu, insan beynine benzeyen katmanlı bir yapıda birbirine bağlı
düğümleri veya nöronları kullanan ve derin öğrenme adı verilen bir tür makine öğrenimi
sürecidir. Bilgisayarların hatalarından ders çıkarmak ve sürekli olarak gelişmek için
kullandığı uyarlanabilir bir sistem oluşturur. Böylece, yapay sinir ağları, belgelerin
özetini çıkarma ya da yüzleri tanıma gibi karmaşık sorunları daha fazla doğrulukla
çözmeye çalışır.

![image](https://github.com/user-attachments/assets/30399c04-f585-4c7d-a252-20bf81dce29b)


#### Evrişimli Sinir Ağları : Evrişimli (ya da evrişimsel) sinir ağları (Convolutional Neural Networks, CNN) görüntü
işleme, sınıflandırma ve segmentasyonu için en popüler ve güçlü araçtır. Bir evrişimsel
sinir ağı bir girdi görüntüsünü alabilen, görüntüdeki çeşitli nesnelere önem (weight ve
bias) atayan ve nesnelerin birbirinden ayırt edilebilmesini sağlayabilen, aynı zamanda
nesnelerin birbirleriyle olan ilişkilerini çıkarabilen bir derin öğrenme algoritmasıdır

![image](https://github.com/user-attachments/assets/e8603feb-681e-4591-b9b6-1e2f65131167)


## Değerlendirme Metrikleri

Makine öğrenimi ve derin öğrenme modellerinin performansını değerlendirmek için
çeşitli metrikler kullanılır. Bu metrikler, modelin ne kadar iyi genelleme yaptığını, yani
eğitim verileri dışındaki veriler üzerinde ne kadar başarılı olduğunu ölçmek için
önemlidir. Özellikle tıbbi görüntü analizi gibi kritik alanlarda modellerin doğruluğunu ve
güvenilirliğini değerlendirmek hayati önem taşımaktadır.

![image](https://github.com/user-attachments/assets/1a6cfad8-d61b-4e36-8bdb-175bac9b049e)

#### Doğruluk (Accuracy)
Modelin tüm doğru tahminlerinin, toplam tahminlere
oranını ifade eder. Tüm sınıflar göz önünde bulundurularak, doğru sınıflandırılan
örneklerin oranını gösterir.

![image](https://github.com/user-attachments/assets/f6a56fdb-d49c-4d6b-99ce-73b601219c37)

#### Hassasiyet (Precision)
Modelin doğru pozitif tahminlerinin, toplam pozitif tahminlere oranını belirtir. Yani, modelin pozitif sınıf olarak tahmin ettiği
örneklerin ne kadarının gerçekten pozitif olduğunu ölçer.

![image](https://github.com/user-attachments/assets/83501ebe-1050-40e2-b6d5-c80fbc89b33a)

#### Duyarlılık (Recall)
Modelin doğru pozitif tahminlerinin, toplam gerçek pozitif
örneklere oranını ifade eder. Bu metrik, modelin pozitif sınıfı ne kadar iyi tespit ettiğini gösterir.

![image](https://github.com/user-attachments/assets/db488c41-084d-4c12-b651-f8b8d5ecb556)

#### F1 Skoru (F1 Score)
Hassasiyet ve duyarlılığın harmonik ortalaması olup,
özellikle dengesiz veri setlerinde daha anlamlı bir performans ölçütüdür. Hem
yanlış pozitif hem de yanlış negatif tahminleri dikkate alarak genel model
performansını değerlendirir.

![image](https://github.com/user-attachments/assets/5cc160fc-3748-4d73-b72d-6736afadfce2)

## Kullanılan Kütüphaneler
Tensorflow,Keras,Matplotlib,Numpy,cv2(OpenCV),Sklearn,Os,Joblib,Seaborn

# Sonuçlar
## Karar Ağaçları (Decision Tree)
![image](https://github.com/user-attachments/assets/69bc11b3-c2f3-4294-b1c2-f48590b4ac05)

## K-En Yakın Komşu (K-Nearest Neighbors, KNN)
![image](https://github.com/user-attachments/assets/2e2cfdee-fbad-4a76-b927-5b949513cacc)

##  Yapay Sinir Ağları (Artificial Neural Networks, ANN)
![image](https://github.com/user-attachments/assets/4dad2484-cde0-4c8d-aab3-b2e29b545ee4)

## Konvolüsyonel Sinir Ağları (Convolutional Neural Networks, CNN)
![image](https://github.com/user-attachments/assets/6e808fbe-4635-4fce-ad84-e6b13c713088)

## Genel Değerlendirme Ve Karşılaştırma

Bu çalışmada, dört farklı makine öğrenmesi algoritması kullanılarak beyin tümörü teşhisi
üzerine kapsamlı bir analiz yapılmıştır. Karar ağaçları ve KNN, daha basit ve hızlı
uygulanabilir algoritmalar olup, küçük ve orta ölçekli veri kümelerinde makul performans
göstermiştir. Yapay sinir ağları, daha karmaşık veri yapılarını modelleyebilme
yetenekleri ile dikkat çekerken, konvolüsyonel sinir ağları özellikle görüntü verileri
üzerinde en yüksek doğruluk oranlarına ulaşmıştır. Sonuçlar, CNN'nin beyin tümörü
teşhisinde en etkili algoritma olduğunu ve klinik uygulamalarda kullanılabilirliğini
göstermiştir.
Sonuç olarak, makine öğrenmesi ve derin öğrenme algoritmalarının beyin tümörü
teşhisinde önemli bir potansiyele sahip olduğu ve doğru algoritma seçimi ile yüksek
doğruluk oranlarına ulaşılabileceği görülmüştür. Gelecekteki çalışmalar, daha büyük ve
çeşitli veri setleri kullanarak algoritmaların performansını daha da iyileştirebilir ve klinik
uygulamalarda daha yaygın bir şekilde kullanılmasını sağlayabilir.

![image](https://github.com/user-attachments/assets/5648229e-73bd-4813-8608-4dfb420ca515)










