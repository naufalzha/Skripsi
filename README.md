# ANALISIS SENTIMEN MASYARAKAT TEHADAP KEBIJAKAN PPKM PADA MEDIA SOSIAL TWITTER MENGGUNAKAN METODE *NAIVE  BAYES CLASSIFIER (NBC)*

![love](https://img.shields.io/badge/Made%20with-🖤-white)
[![Python](https://img.shields.io/badge/Python-3.7%20|%203.8%20|%203.9-green?logo=python)](https://www.python.org/)

## Abstrak 
Penelitian ini dilakukan untuk menerapkan dan mengetahui bagaimana proses metode Naive Bayes Classifier dalam melakukan analisis sentimen terhadap  tweet tentang PPKM, serta seberapa baik metode bekerja. Selain itu, pada penelitian ini juga akan dilihat topik apa saja yang sering menjadi perbincangan pada setiap sentimen. Penelitian ini menggunakan data sekunder dari PT.Ivonesia Solusi Data (Ivosight)  tahun 2021. Hasil analisis didapatkan bahwa algoritma Naive Bayes Classifier mampu mendapatkan akurasi pada data latih berkisar antara 0,68 hingga 0,71. Sementara itu, tingkat akurasi pada data uji sebesar 0,714. Hasil ini menunjukan bahwa algoritma Naive Bayes Classifier sudah bekerja dengan baik. Adapun beberapa topik utama yang sering diperbincangkan terhadap penerapan kebijakan PPKM adalah penerapan PPKM berlevel, vaksinasi, penerapan sistem kerja dari rumah (WFH) serta pembatasan waktu makan.

[![Word](https://img.shields.io/badge/Microsoft_Word-2B579A?style=for-the-badge&logo=microsoft-word&logoColor=white)](https://drive.google.com/file/d/1y-4NWF2yDkpSpWrykuyitnHZTABMJrk_/view?usp=sharing)
[![PPT](https://img.shields.io/badge/Microsoft_PowerPoint-B7472A?style=for-the-badge&logo=microsoft-powerpoint&logoColor=white)](https://docs.google.com/presentation/d/1gUJb6qbTgtFFgE_aHftQS9AQVKCjOsnn/edit?usp=sharing&ouid=111612960542999672386&rtpof=true&sd=true)

## Dataset 
Kumpulan Dataset yang digunakan.
1. `[Full-Data] PPKM` : Data Awal 
2. `[Data-Cleansing] PPKM` : [![Github](https://img.shields.io/badge/Github-black?logo=github)](https://github.com/naufalzha/Skripsi/blob/main/Data/%5BData-Cleansing%5D%20PPKM.csv) Data yang telah melewati proses sampling, labelling dan cleansing.
3. `[Data-Preprocessing] PPKM` : [![Github](https://img.shields.io/badge/Github-black?logo=github)](https://github.com/naufalzha/Skripsi/blob/main/Data/%5BData-Preprocessing%5D%20PPKM.csv) Data yang telah selesai dilakukan preprocessing.

## Kumpulan Notebook yang digunakan  
Kumpulan Dataset yang digunakan.
1. `[Cleansing Notebook] PPKM` : [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SCyUwgZCjSe6znETuMqXCkzxXyT7b8ra?usp=sharing) Notebook yang digunakan untuk mengakses data awal dan cleansing data 
2. `[Preprocessing Notebook] PPKM` : [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/17y3EehapioFkXcn_71IN1QHz2tdfueO7?usp=sharing) Notebook ini digunakan dalam preprocessing data  
3. `[Modelling Notebook] PPKM` : [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ZqG3mDnwYrgbifgSu6gjb7hF6z26ZgGb?usp=sharing) Notebook ini digunakan dalam membangun model 
4. `[Deskriptif Notebook] PPKM` : [![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1_uH_195DzmL4dERs1UdyhTSHNRaBYL7o?usp=sharing) Notebook ini digunakan dalam proses statistik deskriptif 

## Preprocessing Data 
1. Text Cleansing
2. Case Folding
3. Tokeneizinfg
4. Normalization
5. Steamming 

berikut merupakan hasil yang didapatkan sebelum dan sesudah diterapkanya pre-processing data
| Sebelum      | Sesudah |
| ----------- | ----------- |
| RT @fsskroeppreal: PPKM - Pernah percaya kemudian menyesal.~ https://t.co/GT6k6wPMFb     | 'rt', 'ppkm', 'pernah', 'percaya', 'kemudian', 'sesal'     |
| RT @PolsekPupuan:Cegah Penyebaran Covid-19, Kapolsek Selbar bagikan masker gratis kepada masyarakat di Pasar Surabrata. #masker #pakaimasker #prokes #ppkm #BersatuLawanCorona #polrestabanan https://t.co/d0wDwX2VTi   | 'rt', 'cegah', 'sebar', 'covid', 'kapolsek', 'selbar', 'bagi', 'masker', 'gratis', 'kepada', 'masyarakat', 'di', 'pasar', 'surabrata', 'masker', 'pakaimasker', 'prokes', 'pkm', 'bersatulawancorona', 'polrestabanan'  |
|@Humas_SekMaos Pemerintah merevisi aturan Pemberlakuan Pembatasan Kegiatan Masyarakat (PPKM) Darurat yang diberlakukan sejak 3 Juli 2021.\n#DisiplinSuksesPPKM\nLebih Baik Dirumah | 'sekmaos', 'perintah', 'revisi', 'atur', 'laku', 'batas', 'giat', 'masyarakat', 'pkm', 'darurat', 'yang', 'laku', 'sejak', 'juli', 'disiplinsuksespkm', 'lebih', 'baik', 'rumah' |

## TF - IDF 
menggunakan [TF-IDF](http://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html)

<img src="https://github.com/naufalzha/Skripsi/blob/main/Screenshot%20(1050).png"  width="500" height="500">

## Data Splits dan Cross validation
Data Train 80% (3483) data latih 20% (871), selanjutnya data latih akan di lakukan proses cross validation sebanyak 5 split

## Modelling 

Thank You For Attention! :grin: , See u Next Project :v:

©Naufal Zhafran Albaqi-
