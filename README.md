# de-dsf49-job_salary_prediction
# 💼 Job Salary Data Engineering & Analysis Project

## 📌 Deskripsi Project
Project ini merupakan implementasi end-to-end **Data Engineering dan Data Analysis** menggunakan dataset *Job Salary Prediction* yang berisi sekitar 250.000 data pekerjaan.

Tujuan dari project ini adalah untuk:
- Membersihkan dan memproses data mentah (data cleaning & transformation)
- Menyimpan hasil dalam berbagai format (Excel & SQL)
- Melakukan analisis data untuk memahami faktor-faktor yang mempengaruhi salary
- Menyajikan insight melalui visualisasi

---

## 📊 Dataset
- Sumber: Kaggle
- Jumlah data: ±250.000 records
- Format: CSV

Dataset berisi informasi seperti:
- Job Title
- Experience Years
- Education Level
- Industry
- Company Size
- Location
- Salary

---

## ⚙️ Data Engineering Process

### 1. Data Collection
Dataset diambil dari Kaggle dalam format CSV sebagai raw data.

---

### 2. Data Cleaning & Data Quality Check
Proses yang dilakukan:
- Menghapus missing values (`dropna`)
- Menghapus data duplikat (`drop_duplicates`)
- Normalisasi nama kolom (lowercase & format standar)
- Validasi data (salary > 0)

---

### 3. Data Filtering
Memilih kolom yang relevan untuk analisis:
- job_title
- experience_years
- education_level
- industry
- company_size
- location
- salary

---

### 4. Data Transformation
Menambahkan kolom baru:
- **salary_category**:
  - Low (< 50.000)
  - Medium (50.000 – 100.000)
  - High (> 100.000)

---

### 5. Data Export
Hasil data disimpan dalam:
- 📄 Excel → `cleaned_job_salary.xlsx`
- 🗄️ SQL → `job_salary.sql`

---

## 🛡️ Data Governance

### 📘 Data Dictionary
Data dictionary dibuat untuk menjelaskan struktur dataset:
- Nama kolom
- Tipe data
- Deskripsi

File: `data_dictionary.xlsx`

---

### 🔒 Data Masking
Dataset tidak mengandung data sensitif seperti:
- Nama individu
- Email
- Nomor identitas

Sehingga proses data masking tidak diperlukan.

---

## 📊 Data Analysis & Visualization

Analisis dilakukan menggunakan Python dan menghasilkan beberapa visualisasi:

### 📈 1. Salary vs Experience
Menunjukkan hubungan antara pengalaman kerja dan rata-rata salary.

### 📊 2. Top 10 Job dengan Salary Tertinggi
Mengidentifikasi pekerjaan dengan rata-rata gaji tertinggi.

### 🏢 3. Salary per Industry
Membandingkan rata-rata gaji antar industri.

### 📉 4. Distribusi Salary
Melihat pola distribusi gaji dalam dataset.

---

## 📈 Insight & Interpretasi

Berdasarkan hasil analisis:

- Pengalaman kerja memiliki korelasi positif terhadap peningkatan salary  
- Semakin tinggi pengalaman, rata-rata gaji cenderung meningkat  
- Terdapat variasi signifikan antar job title dan industri  
- Beberapa industri menawarkan gaji lebih tinggi dibandingkan lainnya  

Hal ini menunjukkan bahwa salary dipengaruhi oleh kombinasi faktor:
- pengalaman kerja
- jenis pekerjaan
- sektor industri

---

## 🛠️ Tools & Teknologi
- Python
- Pandas
- Matplotlib
- Jupyter Notebook
- GitHub

---

## 📁 Struktur Project
- job_salary_prediction_dataset.csv
- job_salary_data_engineering.ipynb
- job_salary_analysis.ipynb
- cleaned_job_salary.xlsx
- job_salary.sql
- data_dictionary.xlsx
- README.md

---

## 🚀 Cara Menjalankan Project
```bash
1. Clone repository:
git clone <repo-url>
2. Install dependencies:
pip install pandas openpyxl matplotlib
3. Jalankan notebook:
job_salary_data_engineering.ipynb
job_salary_analysis.ipynb
