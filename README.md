# Pertemuan 13 - Debugging dan Testing

Nama: Inayatul Sholihah
NIM: 2225250057
Kelas: PMAT A

## Kasus
Program yang diuji adalah program untuk menghitung rata-rata nilai, menentukan status kelulusan, dan mencari nilai tertinggi.

## Test Case

| ID | Input | Expected | Actual Awal | Status |
|---|---|---|---|---|
| T1 | [80, 60, 90, 70] | 75.0 | 60.0 | FAIL |
| T2 | [100, 80] | 90.0 | 36.0 | FAIL |
| T3 | 60 | Lulus | Tidak lulus | FAIL |
| T4 | 59 | Tidak lulus | Tidak lulus | PASS |
| T5 | [80, 60, 90, 70] | 90 | 0 | FAIL |

## Bug Report
1. Bug rata-rata: pembagian menggunakan angka 5, bukan jumlah data.
2. Bug status kelulusan: kondisi menggunakan `nilai > 60`, seharusnya `nilai >= 60`.
3. Bug nilai tertinggi: kondisi menggunakan `x < tertinggi`, seharusnya `x > tertinggi`.

## Retest

| ID | Input | Expected | Actual Setelah Perbaikan | Status |
|---|---|---|---|---|
| T1 | [80, 60, 90, 70] | 75.0 | 75.0 | PASS |
| T2 | [100, 80] | 90.0 | 90.0 | PASS |
| T3 | 60 | Lulus | Lulus | PASS |
| T4 | 59 | Tidak lulus | Tidak lulus | PASS |
| T5 | [80, 60, 90, 70] | 90 | 90 | PASS |

## Cara Menjalankan
python3 praktik/praktik_4_debugging.py

## Refleksi

Teknik debugging yang paling membantu adalah menggunakan test case dan melihat hasil keluaran program. Dengan test case, kesalahan pada program dapat diketahui dengan membandingkan hasil aktual dan hasil yang diharapkan. Setelah kode diperbaiki, program diuji kembali untuk memastikan semua test case berhasil.