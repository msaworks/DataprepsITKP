# Pemetaan Dataset Pengadaan (Sample V2)

Dokumen ini memetakan keterkaitan antar-sampel dataset pengadaan yang terdapat pada `Docs/consolidated_datasamplesV2.json`. Ringkasan disusun untuk membantu penelusuran metode pengadaan, jumlah paket, tahapan proses, cara pengadaan, serta detail sumber dana dari setiap kelompok data.

## Ringkasan Tingkat-Atas

- **Metode pengadaan yang muncul**: Pengadaan Langsung, E-Purchasing, Seleksi, dan Tender (dari data RUP); metode evaluasi/kualifikasi tender meliputi Harga Terendah Sistem Gugur, Kualitas dan Biaya, Pasca Satu File, dan Pra Dua File Kualitas Biaya.【F:Docs/consolidated_datasamplesV2.json†L1973-L3219】【F:Docs/consolidated_datasamplesV2.json†L13342-L14039】【F:Docs/consolidated_datasamplesV2.json†L18605-L19566】
- **Jumlah paket per metode (RUP Penyedia)**: Pengadaan Langsung 17 paket, E-Purchasing 3 paket, Seleksi 4 paket, Tender 1 paket. Tidak ada paket yang diberi status "dikecualikan" pada sampel ini.【F:Docs/consolidated_datasamplesV2.json†L1973-L3219】
- **Cara pengadaan**: Paket penyedia (`tipe paket` = Penyedia) dan paket swakelola (`tipe_swakelola` = 1, seluruh sampel).【F:Docs/consolidated_datasamplesV2.json†L1973-L3219】【F:Docs/consolidated_datasamplesV2.json†L12573-L13293】
- **Tahapan proses**: Data RUP menggambarkan tahap perencanaan; data SPSE menggambarkan tahap pengumuman, pelaksanaan tender/non-tender, dan ekontrak; data e-Catalog menggambarkan tahap pemesanan e-purchasing.【F:Docs/consolidated_datasamplesV2.json†L1973-L19566】【F:Docs/consolidated_datasamplesV2.json†L3259-L11081】【F:Docs/consolidated_datasamplesV2.json†L15047-L19566】【F:Docs/consolidated_datasamplesV2.json†L21233-L21733】
- **Sumber dana utama**: APBD mendominasi seluruh sampel dengan kemunculan tambahan BLUD dan APBDP pada beberapa dataset tender/non-tender dan e-Catalog.【F:Docs/consolidated_datasamplesV2.json†L2571-L3903】【F:Docs/consolidated_datasamplesV2.json†L3259-L11081】【F:Docs/consolidated_datasamplesV2.json†L17461-L19566】【F:Docs/consolidated_datasamplesV2.json†L21281-L21683】

## Detail Per Dataset & Hubungan Kunci

| Dataset | Tahap Proses | Metode / Cara Pengadaan | Kunci Relasi Utama | Catatan Tambahan |
| --- | --- | --- | --- | --- |
| **RUP-PaketPenyedia-Terumumkan** (`21_1018_...`) | Perencanaan (RUP Penyedia) | `metode_pengadaan` \= Pengadaan Langsung (17), E-Purchasing (3), Seleksi (4), Tender (1) | `kd_rup`, `kd_satker`, `kd_klpd` | `status_dikecualikan` seluruhnya `false`; menyediakan `alasan_dikecualikan` (kosong) bila diperlukan.【F:Docs/consolidated_datasamplesV2.json†L1973-L3219】 |
| **RUP-PaketAnggaranPenyedia** (`18_1028_...`) | Perencanaan anggaran Penyedia | Mengacu pada paket penyedia (relasi `kd_rup`) | `kd_rup`, `kd_satker`, `mak`, `asal_dana`, `sumber_dana` | Seluruh sampel bersumber dari APBD; `asal_dana` identik `D107` (kode K/L/PD).【F:Docs/consolidated_datasamplesV2.json†L2571-L3233】 |
| **RUP-PaketAnggaranSwakelola** (`19_1033_...`) | Perencanaan anggaran Swakelola | Paket swakelola | `kd_rup`, `kd_satker`, `mak`, `asal_dana`, `sumber_dana` | 24 paket APBD dan 1 paket BLUD; `asal_dana` tetap `D107`.【F:Docs/consolidated_datasamplesV2.json†L3245-L3903】 |
| **RUP-PaketSwakelola-Terumumkan** (`23_1030_...`) | Perencanaan Swakelola | `tipe_swakelola` seluruhnya "1" (Swakelola Tipe I) | `kd_rup`, `kd_satker`, `kd_klpd_penyelenggara` | Menghubungkan ke paket anggaran swakelola melalui `kd_rup`.【F:Docs/consolidated_datasamplesV2.json†L12573-L13293】 |
| **SPSE-TenderPengumuman** (`47_1013_...`) | Persiapan & Pengumuman Tender | `mtd_pemilihan` (Tender 16, Seleksi 9), `mtd_evaluasi`, `mtd_kualifikasi` | `kd_tender`, `kd_rup`, `kd_satker`, `kd_lpse` | Status tender: 17 selesai, 5 gagal/batal, 3 berlangsung; sumber dana APBD/APBDP/BLUD.【F:Docs/consolidated_datasamplesV2.json†L13341-L14039】【F:Docs/consolidated_datasamplesV2.json†L9697-L10180】 |
| **SPSE-TenderSelesai** (`48_1014_...`) | Pelaksanaan Tender (selesai) | `mtd_pemilihan` (Seleksi 15, Tender 10) | `kd_tender`, `kd_rup`, `kd_satker`, `kd_lpse` | Status seluruhnya `Selesai`; sumber dana APBD (24) & BLUD (1); tersedia nilai kontrak dan pagu.【F:Docs/consolidated_datasamplesV2.json†L18604-L19566】 |
| **SPSE-TenderEkontrak-1SPPBJ/2Kontrak/3SPMKSPP** (`46_...`, `44_...`, `45_...`) | Tahap Kontrak Tender | `mtd_pengadaan` (selaras dengan tender), info kontrak & pelaksanaan | `kd_tender`, `kd_satker`, `no_sppbj` / `no_kontrak` | Menyediakan detail penandatanganan, nilai kontrak, jadwal pelaksanaan, dan status kontrak (`Kontrak Sedang Berjalan`).【F:Docs/consolidated_datasamplesV2.json†L14734-L17393】 |
| **SPSE-NonTenderPengumuman/Selesai** (`36_...`, `37_...`) | Pengumuman & Realisasi Non-Tender | `mtd_pemilihan` seluruhnya Pengadaan Langsung | `kd_nontender`, `kd_rup`, `kd_satker`, `kd_lpse` | Menampilkan status paket (Selesai/Berlangsung/Gagal) dan sumber dana APBD/APBDP.【F:Docs/consolidated_datasamplesV2.json†L3259-L5110】【F:Docs/consolidated_datasamplesV2.json†L9388-L10180】 |
| **SPSE-NonTenderEkontrak** (`33_1080_...`, `34_1083_...`, `35_1081_...`, `32_1082_...`) | Tahap Kontrak Non-Tender | `mtd_pengadaan` = Pengadaan Langsung | `kd_nontender`, `no_sppbj`, `no_kontrak` | Menyediakan status kontrak (13 selesai, 12 berjalan) dan detail addendum, nilai jaminan, hingga progres pekerjaan.【F:Docs/consolidated_datasamplesV2.json†L5944-L9387】 |
| **SPSE-PencatatanNonTender & Realisasi** (`38_...`, `39_...`) | Pencatatan & Realisasi Non-Tender | `mtd_pemilihan` = Pengadaan Langsung, `jenis_realisasi` (Surat Perjanjian, Kwitansi, Bukti Pembelian) | `kd_nontender_pct`, `kd_rup` | Mengaitkan informasi realisasi pembayaran dengan paket non-tender dan sumber dana APBD.【F:Docs/consolidated_datasamplesV2.json†L9697-L11081】 |
| **Ecat-PaketEPurchasingV6** (`50_1213_...`) | Pemesanan E-Catalog | Status paket e-purchasing (`ON_PROCESS`, `PAYMENT_OUTSIDE_SYSTEM`) | `kd_paket`, `kd_rup`, `kd_satker`, `kd_penyedia_v6` | Sumber dana campuran APBD (7) dan APBDP (18); nilai total harga & ongkir tersedia.【F:Docs/consolidated_datasamplesV2.json†L21233-L21733】 |

## Korelasi Antar Dataset

1. **Perencanaan ke Pelaksanaan**
   - `kd_rup` menghubungkan paket RUP (penyedia maupun swakelola) dengan pengumuman tender/non-tender SPSE serta paket e-Catalog. Hal ini memungkinkan penelusuran dari rencana awal ke pelaksanaan aktual.【F:Docs/consolidated_datasamplesV2.json†L1973-L19566】【F:Docs/consolidated_datasamplesV2.json†L3259-L11081】【F:Docs/consolidated_datasamplesV2.json†L15047-L19566】【F:Docs/consolidated_datasamplesV2.json†L21233-L21733】
   - `kd_satker` dan `kd_klpd` konsisten di seluruh dataset, memudahkan agregasi berdasarkan satuan kerja atau instansi.【F:Docs/consolidated_datasamplesV2.json†L1973-L19566】【F:Docs/consolidated_datasamplesV2.json†L3259-L11081】【F:Docs/consolidated_datasamplesV2.json†L15047-L19566】【F:Docs/consolidated_datasamplesV2.json†L21233-L21733】

2. **Metode Pengadaan dan Status Dikecualikan**
   - Metode dalam RUP (Pengadaan Langsung, E-Purchasing, Seleksi, Tender) memetakan paket perencanaan. `status_dikecualikan` hadir di RUP-Penyedia; bila `true`, detail alasan tersedia pada `alasan_dikecualikan`. Dalam sampel ini seluruh paket `false`, namun struktur siap untuk klasifikasi "dikecualikan" sebagai sub-kategori metode pengadaan tertentu.【F:Docs/consolidated_datasamplesV2.json†L1973-L3219】
   - Metode pada SPSE (`mtd_pemilihan`, `mtd_evaluasi`, `mtd_kualifikasi`) memperinci cara pemilihan penyedia sesuai jenis paket (tender vs non-tender) dan dapat dipetakan kembali ke `metode_pengadaan` melalui `kd_rup` atau `kd_tender` / `kd_nontender`.【F:Docs/consolidated_datasamplesV2.json†L13341-L14039】【F:Docs/consolidated_datasamplesV2.json†L18604-L19566】

3. **Cara Pengadaan (Penyedia vs Swakelola)**
   - Paket penyedia terwakili oleh RUP Penyedia, SPSE Tender/Non-Tender, dan E-Catalog (melalui `status_pkt`).
   - Paket swakelola tercermin pada RUP Swakelola dan paket anggaran swakelola. Parameter `tipe_swakelola` = 1 menunjukkan penyelenggaraan oleh K/L/PD, dan dapat dikaitkan dengan data pelaksanaan swakelola jika tersedia di sumber lain (belum ada pada sampel ini).【F:Docs/consolidated_datasamplesV2.json†L3245-L3903】【F:Docs/consolidated_datasamplesV2.json†L12573-L13293】

4. **Tahapan Kontrak dan Realisasi**
   - Setelah penetapan pemenang, data ekontrak SPSE (Tender & Non-Tender) menyimpan `status_kontrak`, detail nilai dan jadwal (`tgl_kontrak`, `tgl_mulai_pekerjaan`, `tgl_selesai_pekerjaan`).【F:Docs/consolidated_datasamplesV2.json†L5944-L9387】
   - Data Pencatatan Non-Tender dan Realisasi menyediakan bukti pembayaran (`bukti_pembayaran`, `jenis_realisasi`) yang terhubung ke paket non-tender melalui `kd_nontender_pct` dan `kd_rup`.【F:Docs/consolidated_datasamplesV2.json†L9697-L11081】

5. **Sumber Dana**
   - Sumber dana dapat ditelusuri dari tahap perencanaan anggaran (kolom `sumber_dana` dan `asal_dana`) sampai tahap pelaksanaan (SPSE) dan e-Catalog. Contoh: paket dengan `sumber_dana` = APBD di RUP juga muncul sebagai APBD pada tender/non-tender dan pencatatan realisasi.【F:Docs/consolidated_datasamplesV2.json†L2571-L3903】【F:Docs/consolidated_datasamplesV2.json†L3259-L11081】【F:Docs/consolidated_datasamplesV2.json†L17461-L19566】【F:Docs/consolidated_datasamplesV2.json†L21281-L21683】

## Catatan Penggunaan Data

- Seluruh analisis pada dokumen ini menggunakan sampel dari `Docs/consolidated_datasamplesV2.json`. Tidak ada data tambahan dari folder `RawData_Endpoint` yang digunakan.

