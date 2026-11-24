# ATM: The Impact of LLMs on Code Review Process (Modifikasi dengan RAG & Oracle Vector DB)

    Nama: Rayhan Aghno Zakri Setiawan

    NIM: 12409011030042

    Mata Kuliah: Software Quality Assurance 

    Paper Referensi: 
    - The Impact of Large Language Models (LLMs) on Code Review Process
    - Introduction to Vector Search with Oracle Database 23ai

## Tujuan Eksperimen 

Eksperimen ini bertujuan untuk Melakukan replikasi (Tiru) dan modifikasi (ATM) dari paper referensi. Paper asli meneliti dampak PR yang dibantu GPT terhadap proses code review.

Penelitian juga akan Menggunakan pendekatan Retrieval-Augmented Generation (RAG) dengan Oracle Vector Database 23ai untuk memberikan konteks historical code reviews kepada LLM, agar dapat melihat apakah LLM dapat meningkatkan kualitas review yang dihasilkan.

## Dataset

Dari Paper asli (The Impact of Large Language Models (LLMs) on Code Review Process), terdapat dataset penuh 25.473 PR dari 9.254 proyek GitHub. Eksperimen ini akan menggunakan subset kecil (1-10) yang akan diambil secara acak dari dataset publik Github untuk keperluan evaluasi laboratoriun (dikarenakan keterbatasan komputasi)

## Metodologi 

=> Baseline (Tiru) : Mengirim code snippet (dari PR) ke LLM dengan menggunakan shot prompt standar <br>
=> Modifikasi (RAG) : Mengambil snippet, mencari review historis yang paling mirip dengan Oracle Vector DB, dan memasukkannya sebagai few-shot context ke dalam prompt LLM. <br>
=> Evaluasi : Menghitung perbedaan skor seperti Precision antara Baseline dan RAG <br>

## Struktur Direktori : 

- 01_dataset/ : Berisi sampel data 
- 02_oracle_setup/ : Kode untuk melakukan setup Oracle
- 03_prompts/ : Berisi template prompt (Baseline vs RAG)
- 04_code/ : Kode Python untuk eksekusi eksperimen dan koneksi ke Oracle
- 05_Hasil/ : Hasil evaluasi dan analisis statistik
- Bahan Bacaan/ : Referensi Sumber Oracle dan Paper Wajib
- Dokumentasi/ : Print Screen atau catatan yang relevan
