# Resume Data Pengadaan (Dataset Produksi)

Dokumen ini merangkum kondisi riil paket pengadaan berdasarkan dataset produksi pada folder `RawData_Endpoint` yang digunakan pada sampel `Docs/consolidated_datasamplesV2.json`. Fokusnya adalah ketercakupan tahapan (perencanaan hingga serah terima), persebaran metode pengadaan, cara pengadaan (Penyedia/Swakelola), dan referensi sumber dana agar dapat dijadikan _source of truth_.

## Ikhtisar

- Data perencanaan RUP memuat 12.013 paket penyedia dan 5.555 paket swakelola yang sudah diumumkan, dengan dominasi metode Pengadaan Langsung dan E-Purchasing; 641 paket ditandai sebagai dikecualikan namun tetap tercatat sebagai metode tersendiri.【F:RawData_Endpoint/21_1018_RUP-PaketPenyedia-Terumumkan.json†L1-L12013】【F:RawData_Endpoint/23_1030_RUP-PaketSwakelola-Terumumkan.json†L1-L5555】
- Tahap persiapan hingga pemilihan pada SPSE menampung 2.386 paket non-tender dan 92 paket tender dalam pengumuman, serta 1.868 paket non-tender, 68 paket tender, dan 606 paket e-Catalog yang telah melalui pemilihan.【F:RawData_Endpoint/36_1016_SPSE-NonTenderPengumuman.json†L1-L2386】【F:RawData_Endpoint/47_1013_SPSE-TenderPengumuman.json†L1-L92】【F:RawData_Endpoint/37_1017_SPSE-NonTenderSelesai.json†L1-L1868】【F:RawData_Endpoint/48_1014_SPSE-TenderSelesai.json†L1-L68】【F:RawData_Endpoint/50_1213_Ecat-PaketEPurchasingV6.json†L1-L606】
- Tahap kontrak tercatat untuk 1.295 paket non-tender (didominasi Pengadaan Langsung) dan 52 paket tender; sedangkan tahap serah terima baru tersedia untuk 304 paket non-tender karena berkas BAP/BAST tender kosong pada dump ini.【F:RawData_Endpoint/33_1080_SPSE-NonTenderEkontrak-2Kontrak.json†L1-L1047】【F:RawData_Endpoint/35_1081_SPSE-NonTenderEkontrak-1SPPBJ.json†L1-L1302】【F:RawData_Endpoint/34_1083_SPSE-NonTenderEkontrak-3SPMKSPP.json†L1-L965】【F:RawData_Endpoint/44_1073_SPSE-TenderEkontrak-2Kontrak.json†L1-L52】【F:RawData_Endpoint/46_1075_SPSE-TenderEkontrak-1SPPBJ.json†L1-L47】【F:RawData_Endpoint/45_1077_SPSE-TenderEkontrak-3SPMKSPP.json†L1-L45】【F:RawData_Endpoint/32_1082_SPSE-NonTenderEkontrak-4BAPBAST.json†L1-L863】【F:RawData_Endpoint/43_1076_SPSE-TenderEkontrak-4BAPBAST.json†L1-L1】

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

## Ringkasan Tahap vs Cara Pengadaan

| Tahap | Cara | Paket Unik | Catatan |
| --- | --- | --- | --- |
| Perencanaan | Penyedia | 12.013 | Metode dominan Pengadaan Langsung (8.483 paket) dan E-Purchasing (2.661); pagu total Rp1,73T.【F:RawData_Endpoint/21_1018_RUP-PaketPenyedia-Terumumkan.json†L1-L12013】|
| Perencanaan | Swakelola | 5.555 | Mayoritas tipe swakelola I (5.474 paket) dengan total pagu Rp1,05T.【F:RawData_Endpoint/23_1030_RUP-PaketSwakelola-Terumumkan.json†L1-L5555】|
| Persiapan | Penyedia | 2.478 | 2.386 paket Non-Tender (99,96% Pengadaan Langsung) dan 92 paket Tender/Seleksi diumumkan; status masih campuran selesai/berlangsung/gagal.【F:RawData_Endpoint/36_1016_SPSE-NonTenderPengumuman.json†L1-L2386】【F:RawData_Endpoint/47_1013_SPSE-TenderPengumuman.json†L1-L92】|
| Pemilihan | Penyedia | 2.542 | 1.868 paket Non-Tender (1422 selesai), 68 paket Tender selesai, serta 606 paket e-Catalog (516 `ON_PROCESS`, 17 selesai).【F:RawData_Endpoint/37_1017_SPSE-NonTenderSelesai.json†L1-L1868】【F:RawData_Endpoint/48_1014_SPSE-TenderSelesai.json†L1-L68】【F:RawData_Endpoint/50_1213_Ecat-PaketEPurchasingV6.json†L1-L606】|
| Kontrak | Penyedia | 1.347 | 1.295 paket Non-Tender memiliki dokumen SPPBJ/SPMK/kontrak (99,9% Pengadaan Langsung); 52 paket Tender memiliki kontrak namun tidak menyimpan `mtd_pengadaan` pada dump ini.【F:RawData_Endpoint/35_1081_SPSE-NonTenderEkontrak-1SPPBJ.json†L1-L1302】【F:RawData_Endpoint/33_1080_SPSE-NonTenderEkontrak-2Kontrak.json†L1-L1047】【F:RawData_Endpoint/34_1083_SPSE-NonTenderEkontrak-3SPMKSPP.json†L1-L965】【F:RawData_Endpoint/44_1073_SPSE-TenderEkontrak-2Kontrak.json†L1-L52】|
| Serah Terima | Penyedia | 304 | Non-Tender menampilkan 863 catatan BAP/BAST untuk 304 paket, seluruhnya metode Pengadaan Langsung; berkas tender BAP/BAST kosong pada dump (0 byte).【F:RawData_Endpoint/32_1082_SPSE-NonTenderEkontrak-4BAPBAST.json†L1-L863】【F:RawData_Endpoint/43_1076_SPSE-TenderEkontrak-4BAPBAST.json†L1-L1】|

> Tidak ada data pelaksanaan/kontrak untuk swakelola dalam dump ini sehingga tahapan setelah perencanaan hanya mencakup cara pengadaan Penyedia.

## Ringkasan Metode Pengadaan

| Metode | Perencanaan (RUP Penyedia) | Persiapan (SPSE Pengumuman) | Pemilihan (SPSE Selesai & e-Catalog) | Kontrak (SPSE Ekontrak) | Serah Terima |
| --- | --- | --- | --- | --- | --- |
| Pengadaan Langsung | 8.483 paket / Rp565,6M | 2.385 paket | 1.867 paket | 1.294 paket | 304 paket (863 catatan BAP/BAST) |
| E-Purchasing | 2.661 paket / Rp955,1M | – | 606 paket e-Catalog (`ON_PROCESS`: 516, selesai: 17) | – | – |
| Penunjukan Langsung | 142 paket / Rp17,1M | 1 paket | 1 paket | 1 paket | – |
| Tender | 55 paket / Rp126,6M | 56 paket | 42 paket | 52 paket (metode tidak tersimpan) | – |
| Seleksi | 31 paket / Rp13,1M | 36 paket | 26 paket | – | – |
| Dikecualikan | 641 paket / Rp51,6M | – | – | – | – |

Keterangan:
- Nilai pagu berasal dari agregasi kolom `pagu` pada RUP Penyedia.【F:RawData_Endpoint/21_1018_RUP-PaketPenyedia-Terumumkan.json†L1-L12013】
- Paket E-Purchasing di tahap pemilihan seluruhnya bersumber dari `50_1213_Ecat-PaketEPurchasingV6.json` dan mewarisi metode `E-Purchasing` secara implisit.【F:RawData_Endpoint/50_1213_Ecat-PaketEPurchasingV6.json†L1-L606】

## Status Dikecualikan

- 641 paket penyedia ditandai `status_dikecualikan = true` (metode `Dikecualikan`), sedangkan 11.372 paket lain `false`. Tidak ada alasan terisi pada dump ini sehingga perlu rujukan lanjutan bila butuh detail pengecualian.【F:RawData_Endpoint/21_1018_RUP-PaketPenyedia-Terumumkan.json†L1-L12013】

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
