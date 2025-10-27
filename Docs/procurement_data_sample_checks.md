# Uji Sampel Paket Pengadaan

Dokumen ini memverifikasi pemetaan metode dan tahapan pengadaan menggunakan 10 paket contoh. Kolom utama diambil dari sampel `Docs/consolidated_datasamplesV2.json`, sedangkan detail pendanaan dilengkapi dengan referensi silang ke dataset produksi di `RawData_Endpoint` ketika tidak tersedia pada sampel.

## 1. Sepuluh Paket Berdasarkan Metode Pengadaan

| # | Metode | Nama Satker | KD RUP | Pagu | Sumber Dana | Thn Dana | Status RUP | _event_date | Tipe | Volume | Uraian | Status Dikecualikan | Dataset |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Pengadaan Langsung | DINAS KETENAGAKERJAAN | 53605662 | 79,691,100 | APBD | 2025 | Terumumkan | 2025-10-03 | Penyedia | 1 Paket | Belanja Jasa Instruktur, Petugas Rekrut, Iuran Kecelakaan, Uang saku peserta,… | False | Docs/consolidated_datasamplesV2.json -> 21_1018_RUP-PaketPenyedia-Terumumkan (content index 0); RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json |
| 2 | E-Purchasing | BADAN PENDAPATAN DAERAH | 53607461 | 100,000,000 | APBD | 2025 | Terumumkan | 2025-10-03 | Penyedia | 1 Paket | Belanja Jasa Konsultansi Perencanaan Rekayasa-Jasa Desain Rekayasa untuk Kons… | False | Docs/consolidated_datasamplesV2.json -> 21_1018_RUP-PaketPenyedia-Terumumkan (content index 1); RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json |
| 3 | E-Purchasing | BADAN PENDAPATAN DAERAH | 53607638 | 75,000,000 | APBD | 2025 | Terumumkan | 2025-10-03 | Penyedia | 1 Kegiatan | Belanja Jasa Konsultansi Non Konstruksi | False | Docs/consolidated_datasamplesV2.json -> 21_1018_RUP-PaketPenyedia-Terumumkan (content index 2); RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json |
| 4 | Pengadaan Langsung | BADAN PENDAPATAN DAERAH | 53610130 | 15,000,000 | APBD | 2025 | Terumumkan | 2025-10-03 | Penyedia | 1 Kegiatan | Belanja Jasa Tenaga Kesenian dan Kebudayaan | False | Docs/consolidated_datasamplesV2.json -> 21_1018_RUP-PaketPenyedia-Terumumkan (content index 4); RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json |
| 5 | Seleksi | DINAS PEKERJAAN UMUM DAN TATA RUANG | 53613638 | 450,000,000 | APBD | 2025 | Terumumkan | 2025-10-03 | Penyedia | 1 Paket | Perencanaan Rehabilitasi Pembangunan Gedung Kantor Dinas PUTR | False | Docs/consolidated_datasamplesV2.json -> 21_1018_RUP-PaketPenyedia-Terumumkan (content index 5); RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json |
| 6 | Tender | DINAS PEKERJAAN UMUM DAN TATA RUANG | 53613689 | 7,000,000,000 | APBD | 2025 | Terumumkan | 2025-10-03 | Penyedia | 1 Paket | Pembangunan Gedung Kantor Kecamatan Baleendah | False | Docs/consolidated_datasamplesV2.json -> 21_1018_RUP-PaketPenyedia-Terumumkan (content index 7); RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json |
| 7 | Seleksi | DINAS PEKERJAAN UMUM DAN TATA RUANG | 53613698 | 350,000,000 | APBD | 2025 | Terumumkan | 2025-10-03 | Penyedia | 1 Paket | Pengawasan Pembangunan Gedung Kantor Kecamatan Baleendah | False | Docs/consolidated_datasamplesV2.json -> 21_1018_RUP-PaketPenyedia-Terumumkan (content index 8); RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json |
| 8 | Penunjukan Langsung | BADAN PENDAPATAN DAERAH | 53666554 | 100,000,000 | APBD | 2025 | Terumumkan | 2025-10-03 | Penyedia | 1 Kegiatan | Belanja Jasa Konsultansi Berorientasi Layanan-Jasa Studi Penelitian dan Bantuan Teknik | False | RawData_Endpoint/21_1018_RUP-PaketPenyedia-Terumumkan.json; RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json |
| 9 | Dikecualikan | DINAS PENANAMAN MODAL DAN PELAYANAN TERPADU SATU PINTU | 53728945 | 7,200,000 | APBD | 2025 | Terumumkan | 2025-10-03 | Penyedia | 12 Bulan | Belanja Tagihan telepon | True | RawData_Endpoint/21_1018_RUP-PaketPenyedia-Terumumkan.json; RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json |
| 10 | Dikecualikan | DINAS PENANAMAN MODAL DAN PELAYANAN TERPADU SATU PINTU | 53729094 | 60,732,500 | APBD | 2025 | Terumumkan | 2025-10-03 | Penyedia | 7145M3 | Belanja Tagihan Air | True | RawData_Endpoint/21_1018_RUP-PaketPenyedia-Terumumkan.json; RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json |

## 2. Ringkasan Jumlah Paket per Tahap Proses

| Tahap | Paket Penyedia | Paket Swakelola | Dataset utama |
| --- | --- | --- | --- |
| Perencanaan | 25 | 25 | RUP Penyedia (21_1018) & RUP Swakelola (23_1030) |
| Persiapan | 50 | 0 | SPSE Non-Tender Pengumuman (36_1016) + SPSE Tender Pengumuman (47_1013) |
| Pemilihan | 50 | 0 | SPSE Non-Tender Selesai (37_1017) + SPSE Tender Selesai (48_1014) |
| Kontrak | 50 | 0 | SPSE Non-Tender Ekontrak-2Kontrak (33_1080) + SPSE Tender Ekontrak-2Kontrak (44_1073) |
| Serah Terima | 45 | 0 | SPSE Non-Tender Ekontrak-4BAPBAST (32_1082) + SPSE Tender Ekontrak-4BAPBAST (43_1076) |

## 3. Catatan Sumber Data Tambahan

- Field `sumber_dana` dan `tahun_anggaran_dana` tidak tersedia pada sampel `21_1018_RUP-PaketPenyedia-Terumumkan`; keduanya diambil dari pasangan data anggaran di `RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json` menggunakan kunci `kd_rup` yang sama.
- Contoh untuk metode "Penunjukan Langsung" serta paket dengan `status_dikecualikan = true` hanya ditemukan pada data produksi `RawData_Endpoint/21_1018_RUP-PaketPenyedia-Terumumkan.json`, sehingga baris 8–10 di tabel menggunakan sumber tersebut.
- Seluruh agregasi tahap proses pada Tabel 2 bersumber dari sampel `Docs/consolidated_datasamplesV2.json`; setiap dataset SPSE dihitung berdasarkan jumlah unik `kd_nontender` atau `kd_tender` sesuai tahapannya.
