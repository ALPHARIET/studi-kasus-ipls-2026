# Studi Kasus — Informatics Practitioner Lecture Series 2026

Kumpulan **6 studi kasus + implementasi Google Colab** berdasarkan materi para pemateri *Informatics Practitioner
Lecture Series 2026* — Program Studi Informatika, Universitas Bengkulu, bertema
*"Connecting Academic Knowledge with Industry and Global Technology"*.

Setiap notebook berisi: identitas & ringkasan materi pemateri → latar belakang studi kasus → rumusan masalah & tujuan →
implementasi kode langkah demi langkah → analisis hasil → kesimpulan & keterbatasan.

## Daftar studi kasus

| No | Materi & pemateri | Studi kasus | Teknik utama | Notebook |
|---|---|---|---|---|
| 1 | **Make Sense of Data with Analysis and AI** — Andria Arisal (BRIN) · [video](https://www.youtube.com/live/WeIWNNO5vbk) | PT Maju Bersama: omzet naik, laba turun, piutang membengkak | CRISP-DM, *data quality rule engine*, jebakan *join fan-out*, analitik deskriptif–diagnostik–prediktif–preskriptif, *data leakage*, data tidak seimbang, GenAI yang aman | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ALPHARIET/studi-kasus-ipls-2026/blob/main/notebooks/01_make_sense_of_data_analytics_ai.ipynb) |
| 2 | **Bridging Global Infrastructure to Address Local Challenge with HPC** — Asst. Prof. Dr. Worawan Diaz Carballo (Thammasat University) · [video](https://www.youtube.com/live/qeWpf9uXBqE) | Simulasi berbasis agen konsumsi listrik gedung kampus & uji kebijakan hemat energi | FLOPS & mini-LINPACK, presisi *floating point*, Monte Carlo paralel, *speedup*, Hukum Amdahl, *batch script* SLURM | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ALPHARIET/studi-kasus-ipls-2026/blob/main/notebooks/02_hpc_simulasi_energi_gedung_kampus.ipynb) |
| 3 | **Career and Competition in Industrial Era with GIS** — Widi Prima Deva (Citycare Property, Selandia Baru) · [video](https://www.youtube.com/live/TkXkx7HKTto) | Pemilihan lokasi gerai minimarket di Kota Bengkulu, rute logistik, manajemen aset PJU | GeoPandas, proyeksi UTM, *buffer/overlay/spatial join/nearest*, analisis multikriteria + uji sensitivitas, TSP 2-opt, QC survei GNSS, Folium, GeoPackage | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ALPHARIET/studi-kasus-ipls-2026/blob/main/notebooks/03_gis_lokasi_gerai_dan_manajemen_aset.ipynb) |
| 4 | **Introduction to Machine Learning** — Dr. Taniza Tajuddin (UiTM Kedah, Malaysia) · [video bagian 1](https://www.youtube.com/live/FTf9eiE1Tw0) & [bagian 2](https://www.youtube.com/live/0LFeuSypYro) | "Bank Daerah Bengkulu Digital": 8 kebutuhan yang mewakili semua jenis ML | *rule-based* vs ML, regresi harga rumah, klasifikasi pinjaman, K-Means + PCA, Isolation Forest, *association rule*, semi-supervised, Q-learning | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ALPHARIET/studi-kasus-ipls-2026/blob/main/notebooks/04_pengantar_machine_learning.ipynb) |
| 5 | **Human-Computer Interaction & Data Visualization** — Dr. Arafat Febriandirza (BRIN) · [video](https://www.youtube.com/live/5KhQm8OaYRM) | Merancang ulang *dashboard* penjualan UMKM Provinsi Bengkulu untuk persona "Budi" | Persona & skenario, kebutuhan (non)fungsional, *chartjunk*/*data-ink*, atribut pre-atentif, Gestalt, *lie factor*, kontras WCAG, simulasi buta warna, Plotly (mantra Shneiderman), heuristik Nielsen, SUS | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ALPHARIET/studi-kasus-ipls-2026/blob/main/notebooks/05_imk_visualisasi_dashboard_umkm.ipynb) |
| 6 | **Attributing Direct Drivers to Deforestation Alerts with Satellite Imagery and AI** — Dr. Bart Slagter (Wageningen University & Research) · [video](https://www.youtube.com/live/OFLzys5FYqg) | Atribusi pemicu langsung alert deforestasi di bentang alam sekitar TNKS & prioritas patroli | Citra Sentinel-1/2 (sintetis), *benchmark* Random Forest vs **CNN (PyTorch)**, macro-F1, kelas "tidak yakin", ablasi radar vs optik saat berawan, pemilahan ukuran & *hotspot*, indeks musiman, integrasi batas kawasan | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ALPHARIET/studi-kasus-ipls-2026/blob/main/notebooks/06_atribusi_pemicu_deforestasi_cnn.ipynb) |

> Tombol **Open in Colab** di atas mengarah ke `github.com/ALPHARIET/studi-kasus-ipls-2026`. Jika nama akun atau
> repositori GitHub berbeda, ganti bagian `ALPHARIET/studi-kasus-ipls-2026` di README ini.

## Cara menjalankan

**Google Colab (disarankan):** klik tombol *Open in Colab* → `Runtime` → `Run all`. Semua pustaka yang dipakai
(numpy, pandas, scikit-learn, matplotlib, seaborn, plotly, geopandas, folium, PyTorch) sudah tersedia di Colab, jadi
tidak perlu `pip install`. Untuk notebook 6, `Runtime → Change runtime type → GPU` mempercepat pelatihan CNN
(di CPU pun selesai ±3–5 menit).

**Lokal:**

```bash
pip install -r requirements.txt
jupyter lab notebooks/
```

## Catatan penting

* **Semua data bersifat sintetis** — dibangkitkan di dalam notebook dengan *random seed* tetap, sehingga hasil dapat
  direproduksi tanpa mengunduh dataset atau akun khusus (mis. Google Earth Engine). Pola di dalam data sengaja
  dirancang meniru kasus yang dijelaskan para pemateri; angka-angkanya **bukan data resmi**.
* Ringkasan materi disusun dari rekaman siaran langsung di kanal YouTube *Informatika Unib Official*. Nama dan
  istilah diambil dari transkrip otomatis, jadi mohon dicek ulang bila ada ejaan yang keliru.
* Notebook sudah dijalankan dan disimpan **beserta output-nya**, sehingga tabel & grafik langsung terlihat di GitHub.
  Grafik interaktif Plotly/Folium hanya tampil saat dibuka di Colab/Jupyter.

## Struktur repositori

```
studi-kasus-ipls-2026/
├── README.md
├── requirements.txt
└── notebooks/
    ├── 01_make_sense_of_data_analytics_ai.ipynb
    ├── 02_hpc_simulasi_energi_gedung_kampus.ipynb
    ├── 03_gis_lokasi_gerai_dan_manajemen_aset.ipynb
    ├── 04_pengantar_machine_learning.ipynb
    ├── 05_imk_visualisasi_dashboard_umkm.ipynb
    └── 06_atribusi_pemicu_deforestasi_cnn.ipynb
```
