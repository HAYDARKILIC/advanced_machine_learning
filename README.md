# Advanced Machine Learning

Bu repository, İleri Makine Öğrenmesi dersine ait Jupyter Notebook'larını
içermektedir. Her notebook, teorik ders sunumuna eşlik eden uygulamalı Python
çalışmasıdır: slayttaki formüller adım adım türetilir, ardından NumPy ile
sıfırdan kodlanır ve teorinin gerçekten iddia ettiği şeyi yapıp yapmadığı bir
deneyle sınanır.

Notebook'lar **tek başına çalışır**. Her birinin başındaki "toolkit" hücresi, o
derste kullanılan tüm implementasyonları içerir; harici bir paket kurmanız
gerekmez. Gereken tek şey NumPy, SciPy ve Matplotlib'dir.

---

## İçerik

| # | Notebook | Türetilen ve kodlanan konular |
|---|----------|-------------------------------|
| 01 | [İstatistiksel Öğrenme Teorisi](01_statistical_learning_theory.ipynb) | Ampirik risk, yanlılık–varyans ayrışımı, etkin serbestlik derecesi, öğrenme eğrileri, iç içe çapraz doğrulama ve model seçim yanlılığı |
| 02 | [Düzenlileştirme ve Seyreklik](02_regularization_and_sparsity.ipynb) | SVD tabanında ridge büzülmesi, lasso alt-gradyan/KKT koşulları, koordinat inişi – ISTA – FISTA karşılaştırması, elastic net gruplama etkisi |
| 03 | [Çekirdek Yöntemleri](03_kernel_methods.ipynb) | RKHS ve temsil teoremi, Mercer/PSD kontrolü, SMO ile çözülen C-SVM duali, kernel ridge, kernel PCA |
| 04 | [Gauss Süreçleri](04_gaussian_processes.ipynb) | GP önsel ve sonsalı, analitik gradyanlarla log marjinal olabilirlik, Occam usturası olarak kanıt, ARD ile öznitelik önemi, hata çubuklarının kalibrasyonu |
| 05 | [EM ve Gizli Değişkenli Modeller](05_em_latent_variables.ipynb) | ELBO ve EM'in monotonluğu, GMM E/M adımları, yerel optimumlar ve başlangıç seçimi, BIC/AIC ile model seçimi |
| 06 | [Gradyan Artırma](06_gradient_boosting.ipynb) | İkinci mertebe (Newton) boosting, bölme kazancı ve yaprak değeri formülleri, büzülme, alt-örnekleme, erken durdurma, bagging–boosting karşılaştırması |
| 07 | [Otomatik Türev ve Geri Yayılım](07_autodiff_and_backprop.ipynb) | Ters mod otomatik türev, gradyan kontrolü, SGD/momentum/RMSProp/Adam/AdamW, ısınmalı kosinüs öğrenme oranı |
| 08 | [Uyumlu Tahmin (Conformal Prediction)](08_conformal_prediction.ipynb) | Bölünmüş uyumlu tahmin, uyumluluk kuantili, normalize skorlarla uyarlanabilir aralıklar, tahmin kümeleri, marjinal ve koşullu geçerlilik |

Her notebook, bir sonrakine bağlanan kısa bir "what to take away" bölümüyle
biter; sırayla okunduğunda kapasite, belirsizlik ve optimizasyon üzerine tek bir
bütünlüklü anlatı oluştururlar.

## Kullanım

```bash
git clone https://github.com/HAYDARKILIC/advanced_machine_learning.git
cd advanced_machine_learning
pip install numpy scipy matplotlib jupyterlab
jupyter lab
```

Notebook'lar çıktıları çalıştırılmış halde yüklenmiştir; GitHub üzerinden
doğrudan okunabilir ya da "Restart & Run All" ile baştan üretilebilir.

## Not

Kod hücrelerindeki implementasyonlar (SMO, GP marjinal olabilirlik gradyanları,
otomatik türev motoru, ikinci mertebe boosting ağaçları vb.) doğruluk testlerinden
geçirilmiştir: SMO çözümü referans bir SVM uygulamasıyla aynı destek vektörlerini
ve karar fonksiyonunu vermekte, GP ve otomatik türev gradyanları merkezi sonlu
farklarla, EM'in monotonluğu ve uyumlu tahminin kapsama oranı ise doğrudan sayısal
olarak doğrulanmaktadır.

## Kaynaklar

* Hastie, Tibshirani & Friedman, *The Elements of Statistical Learning*, 2. baskı, 2009.
* Bishop, *Pattern Recognition and Machine Learning*, 2006.
* Rasmussen & Williams, *Gaussian Processes for Machine Learning*, 2006.
* Platt, "Sequential Minimal Optimization", MSR-TR-98-14, 1998.
* Chen & Guestrin, "XGBoost: A Scalable Tree Boosting System", KDD 2016.
* Tipping & Bishop, "Probabilistic Principal Component Analysis", JRSS-B, 1999.
* Loshchilov & Hutter, "Decoupled Weight Decay Regularization", ICLR 2019.
* Angelopoulos & Bates, "A Gentle Introduction to Conformal Prediction", 2023.

## Lisans

MIT
