# Resume Data Pengadaan (Dataset Produksi)

Dokumen ini merangkum kondisi riil paket pengadaan berdasarkan dataset produksi pada folder `RawData_Endpoint` yang digunakan pada sampel `Docs/consolidated_datasamplesV2.json`. Fokusnya adalah ketercakupan tahapan (perencanaan hingga serah terima), persebaran metode pengadaan, cara pengadaan (Penyedia/Swakelola), dan referensi sumber dana agar dapat dijadikan _source of truth_.

## Ikhtisar

- Total 17.568 paket produksi yang terdaftar pada RUP (12.013 penyedia + 5.555 swakelola) milik 67 satker dengan nilai pagu kumulatif Rp2.779.495.121.250.【e51f6c†L1-L19】【01a3d6†L1-L2】【01a3d6†L10-L10】
- Resume tahap menunjukkan nilai realisasi terbesar masih berada di perencanaan (Rp2,78T), sementara pemilihan mencakup Rp506,31M termasuk Rp189,68M transaksi e-Catalog.【e51f6c†L1-L7】【01a3d6†L5-L7】
- Data kontrak valid untuk 1.084 paket penyedia (non-tender dan tender) senilai Rp199,65M dan serah terima tercatat untuk 304 paket non-tender dengan pembayaran Rp59,29M akibat absennya berkas BAP/BAST tender.【e51f6c†L1-L7】【01a3d6†L8-L10】【F:RawData_Endpoint/43_1076_SPSE-TenderEkontrak-4BAPBAST.json†L1-L1】

## Sumber Dataset & Kunci

| Tahap | Cara | File Produksi | Kunci Paket | Atribut Tahapan Penting |
| --- | --- | --- | --- | --- |
| Perencanaan | Penyedia | `21_1018_RUP-PaketPenyedia-Terumumkan.json` | `kd_rup`, `kd_satker` | `metode_pengadaan`, `status_umumkan_rup`, `status_dikecualikan`, `pagu`, `_event_date` |
| Perencanaan | Swakelola | `23_1030_RUP-PaketSwakelola-Terumumkan.json` | `kd_rup`, `kd_satker` | `tipe_swakelola`, `tgl_buat_paket`, `pagu`, `_event_date` |
| Persiapan | Penyedia (Non-Tender) | `36_1016_SPSE-NonTenderPengumuman.json` | `kd_nontender`, `kd_rup`, `kd_satker` | `mtd_pemilihan`, `status_nontender`, `tgl_pengumuman_nontender` |
| Persiapan | Penyedia (Tender) | `47_1013_SPSE-TenderPengumuman.json` | `kd_tender`, `kd_rup`, `kd_satker` | `mtd_pemilihan`, `mtd_evaluasi`, `status_tender`, `tgl_pengumuman_tender` |
| Pemilihan | Penyedia (Non-Tender) | `37_1017_SPSE-NonTenderSelesai.json` | `kd_nontender`, `kd_rup` | `mtd_pemilihan`, `status_nontender`, `nilai_kontrak`, `tgl_penetapan_pemenang` |
| Pemilihan | Penyedia (Tender) | `48_1014_SPSE-TenderSelesai.json` | `kd_tender`, `kd_rup` | `mtd_pemilihan`, `status_tender`, `nilai_kontrak`, `tgl_penetapan_pemenang` |
| Pemilihan | Penyedia (e-Catalog) | `50_1213_Ecat-PaketEPurchasingV6.json` | `kd_paket`, `kd_rup`, `kd_satker` | `status_pkt`, `tgl_order`, `sumber_dana`, `total_harga` |
| Kontrak | Penyedia (Non-Tender) | `35_1081`, `33_1080`, `34_1083` SPSE Non-Tender Ekontrak | `kd_nontender`, `no_kontrak` | `mtd_pengadaan`, `status_kontrak`, `tgl_kontrak`, `nilai_kontrak` |
| Kontrak | Penyedia (Tender) | `46_1075`, `44_1073`, `45_1077` SPSE Tender Ekontrak | `kd_tender`, `no_kontrak` | `status_kontrak`, `tgl_kontrak`, `nilai_kontrak` |
| Serah Terima | Penyedia (Non-Tender) | `32_1082_SPSE-NonTenderEkontrak-4BAPBAST.json` | `kd_nontender`, `no_bast` | `mtd_pengadaan`, `tgl_bast`, `besar_pembayaran`, `progres_pekerjaan` |

## Ringkasan Tahap Pengadaan (Produksi)

| Tahap | Jumlah Paket | Nilai (Rp) | Rincian Cara Pengadaan |
| --- | ---: | ---: | --- |
| Perencanaan | 17.568 | 2.779.495.121.250 | Penyedia: 12.013 paket / Rp1.729.137.333.149<br>Swakelola: 5.555 paket / Rp1.050.357.788.101【e51f6c†L1-L7】【01a3d6†L1-L3】|
| Persiapan (Pengumuman) | 2.478 | 426.123.115.030 | Penyedia non-tender: 2.386 paket / Rp255.232.447.694<br>Penyedia tender: 92 paket / Rp170.890.667.336【e51f6c†L2-L4】【01a3d6†L3-L4】|
| Pemilihan | 2.542 | 506.311.524.673,69 | Penyedia non-tender: 1.868 paket / Rp188.816.184.536,81<br>Penyedia tender: 68 paket / Rp127.817.505.347,88<br>E-Purchasing: 606 paket / Rp189.677.834.789【e51f6c†L3-L5】【01a3d6†L4-L7】|
| Kontrak | 1.084 | 199.647.078.151,84 | Penyedia non-tender: 1.032 paket / Rp101.884.179.283,24<br>Penyedia tender: 52 paket / Rp97.762.898.868,60【e51f6c†L5-L6】【01a3d6†L8-L9】|
| Serah Terima | 304 | 59.294.478.841,20 | Penyedia non-tender: 304 paket / Rp59.294.478.841,20 (rekap BAP/BAST); dokumen tender kosong.【e51f6c†L6-L7】【01a3d6†L9-L10】【F:RawData_Endpoint/43_1076_SPSE-TenderEkontrak-4BAPBAST.json†L1-L1】|

> Tahap sesudah perencanaan belum memiliki data swakelola dalam dump produksi, sehingga keseluruhan paket persiapan hingga serah terima berasal dari cara pengadaan penyedia.

## Total Paket, Satker, dan Nilai Pagu RUP

| Metrik | Nilai |
| --- | ---: |
| Total paket (RUP Penyedia + Swakelola) | 17.568 |
| Total satker unik | 67 |
| Total pagu RUP | Rp2.779.495.121.250 |

> Rekap total dihitung dari gabungan dataset RUP penyedia dan swakelola melalui agregasi `kd_satker` serta penjumlahan kolom `pagu`.【e51f6c†L1-L19】

## Ringkasan Metode Pengadaan (RUP Penyedia)

| Metode | Jumlah Paket | Nilai Pagu (Rp) | Catatan |
| --- | ---: | ---: | --- |
| Pengadaan Langsung | 8.483 | 565.599.749.056 | Dominan pada persiapan/pelaksanaan non-tender dan berlanjut hingga serah terima.【e51f6c†L8-L19】|
| Pengadaan Langsung E-Purchasing | 0 | 0 | Tidak ditemukan entri khusus; transaksi katalog tercatat sebagai `E-Purchasing`.【e51f6c†L8-L15】|
| E-Purchasing | 2.661 | 955.146.015.362 | Selaras dengan 606 paket e-Catalog di tahap pemilihan.【e51f6c†L8-L15】【01a3d6†L6-L7】|
| Penunjukan Langsung | 142 | 17.131.471.739 | Nilai kecil, namun berlanjut ke kontrak untuk sebagian paket.【e51f6c†L8-L15】|
| Tender | 55 | 126.565.744.067 | Termasuk tender dan tender cepat pada SPSE.【e51f6c†L8-L15】|
| Seleksi | 31 | 13.110.000.000 | Seluruhnya jasa konsultansi badan usaha.【e51f6c†L8-L15】|
| Dikecualikan | 641 | 51.584.352.925 | 641 paket bertanda `status_dikecualikan = true`; sisanya 11.372 paket `false`.【e51f6c†L8-L17】|

> Nilai pagu metode pengadaan dihitung dari kolom `pagu` RUP Penyedia. Untuk kebutuhan audit, agregasi dilakukan pada `metode_pengadaan` asli; kolom tambahan `status_dikecualikan` menentukan 641 paket pengecualian.

## Status Dikecualikan

- 641 paket penyedia ditandai `status_dikecualikan = true` (metode `Dikecualikan`), sedangkan 11.372 paket lain `false`. Tidak ada alasan terisi pada dump ini sehingga perlu rujukan lanjutan bila butuh detail pengecualian.【e51f6c†L8-L17】

## Ringkasan Sumber Dana

| Sumber | Dataset | Jumlah Catatan | Catatan |
| --- | --- | --- | --- |
| APBD | `18_1028_RUP-PaketAnggaranPenyedia.json` | 13.620 dari 17.115 baris | 12.174 `kd_rup` unik; terdapat multi-baris per paket untuk beberapa kombinasi akun (`mak`).【F:RawData_Endpoint/18_1028_RUP-PaketAnggaranPenyedia.json†L1-L17115】|
| BLUD | `18_1028_RUP-PaketAnggaranPenyedia.json` | 2.247 |  | 
| APBDP | `18_1028_RUP-PaketAnggaranPenyedia.json` | 1.248 |  |
| APBD | `19_1033_RUP-PaketAnggaranSwakelola.json` | 16.050 dari 16.957 baris | 5.633 `kd_rup` unik dengan ragam tipe swakelola; tersedia 558 catatan APBDP dan 314 BLUD.【F:RawData_Endpoint/19_1033_RUP-PaketAnggaranSwakelola.json†L1-L16957】|
| APBD / BLUD / APBDP | `50_1213_Ecat-PaketEPurchasingV6.json` | 391 / 136 / 75 paket | 4 paket mencantumkan kombinasi `APBD,APBDP`; status pesanan mayoritas `ON_PROCESS`.【F:RawData_Endpoint/50_1213_Ecat-PaketEPurchasingV6.json†L1-L606】|

## Catatan Tambahan

- Berkas `43_1076_SPSE-TenderEkontrak-4BAPBAST.json` berukuran 0 byte sehingga tidak tersedia informasi serah terima tender pada dump ini. Validasi lanjutan perlu meminta ulang sumber tersebut apabila dibutuhkan.
- Jumlah paket pada tahap kontrak dihitung berdasarkan union `kd_nontender`/`kd_tender` di tiga berkas ekontrak agar tidak menghitung ganda paket dengan beberapa versi dokumen.
- Tidak ada dataset produksi dalam dump ini yang memuat tahapan pelaksanaan swakelola di luar RUP; analisis lanjutan untuk swakelola membutuhkan sumber tambahan.
