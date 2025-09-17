# 📡 Network Traffic Classification

## Deskripsi
Project ini bertujuan untuk **mendeteksi trafik jaringan abnormal** (anomali) menggunakan machine learning.  
Data yang digunakan hanya memuat informasi trafik jaringan dasar seperti `Duration`, `Protocol`, `SourceIP`, `DestinationIP`, `SourcePort`, `DestinationPort`, `PacketCount`, dan `ByteCount`.  

Tujuan project: memberikan prediksi apakah sebuah trafik jaringan **Normal** atau **Anomali**.  

## Struktur Dataset
| Kolom            | Deskripsi                                      |
|-----------------|-----------------------------------------------|
| Duration        | Durasi koneksi (detik)                         |
| Protocol        | Jenis protokol (TCP, UDP, ICMP, dll)          |
| SourceIP        | Alamat IP sumber                               |
| DestinationIP   | Alamat IP tujuan                               |
| SourcePort      | Port sumber                                    |
| DestinationPort | Port tujuan                                    |
| PacketCount     | Jumlah paket                                   |
| ByteCount       | Jumlah byte                                    |
| Label           | 0 = Normal, 1 = Anomali                        |

## Akurasi Model
| Model                    | Accuracy | Precision | Recall | F1-Score |
| ------------------------ | -------- | --------- | ------ | -------- |
| Support Vector Machine   | 0.5075   | 0.4717    | 0.2618 | 0.3367   |
| Multinomial Naive Bayes  | 0.5075   | 0.4860    | 0.5445 | 0.5136   |
| Random Forest Classifier | 0.5325   | 0.5106    | 0.5026 | 0.5066   |

🔹 Random Forest memiliki performa terbaik dengan F1-Score ~0.51.
🔹 Model masih bisa ditingkatkan melalui feature engineering atau tuning hyperparameter.

## Teknologi
Python 3.10+
Pandas, NumPy, Scikit-learn
Jupyter Notebook
