# Panduan Struktur Data API LKPP

Panduan rinci struktur data dari setiap item pada masing-masing layanan di `daftar_data.json`.

## 1. [1061] Bela-TokoDaringRealisasi

- Kelompok: PURCHASING
- Deskripsi: Data Transaksional Toko Daring
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/da1842e4-e1f8-4a3b-aa01-2a896799ba08/json/5362/Bela-TokoDaringRealisasi/tipe/12:4/parameter/D107:2025`
- Root: list berisi 2 item

- **Struktur Bidang:**
    ```json
{
        "keterangan_ppmse": "str",
        "merchant_name": "null",
        "marketplace": "str",
        "kota_kab": "str",
        "provinsi": "str",
        "kd_satker": "str",
        "sumber_data": "str",
        "status_verif": "str",
        "kd_klpd": "str",
        "kategori": "null",
        "status_konfirmasi_ppmse": "str",
        "nama_klpd": "str",
        "order_id": "str",
        "metode_bayar": "str",
        "tahun": "int",
        "valuasi": "int",
        "jenis_transaksi": "str",
        "nama_pemesan": "str",
        "tanggal_transaksi": "str",
        "nama_satker": "str",
        "order_desc": "null"
    }
    ```

## 2. [1025] Ecat-InstansiSatker

- Kelompok: PURCHASING
- Deskripsi: Detail Dari Instansi berdasarkan Layanan Paket Epurchasing
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/e8f48bc1-165b-4662-8ccf-f6dc857cc0a2/json/5339/Ecat-InstansiSatker/tipe/12/parameter/D107`
- Root: list berisi 336 item

- **Struktur Bidang:**
    ```json
{
        "jenis_klpd": "str",
        "kd_satker": "int",
        "kd_satker_str": "str",
        "nama_klpd": "str",
        "kd_klpd": "str",
        "nama_satker": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `kd_satker_str` memiliki beberapa tipe: `null, str`

## 3. [1021] Ecat-KomoditasDetail

- Kelompok: PURCHASING
- Deskripsi: Detail Dari Komoditas berdasarkan Layanan Paket Epurchasing
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/5e82b63e-601d-4dd3-bb91-f23c43e4d22e/json/5343/Ecat-KomoditasDetail/tipe/4/parameter/567`
- Root: list berisi 1 item

- **Struktur Bidang:**
    ```json
{
        "kd_komoditas": "int",
        "nama_komoditas": "str",
        "kd_instansi_katalog": "str",
        "nama_instansi_katalog": "str",
        "jenis_katalog": "str"
    }
    ```

## 4. [1020] Ecat-PaketEPurchasing

- Kelompok: PURCHASING
- Deskripsi: Layanan Paket Transaksional ePurchasing dari Aplikasi eKatalog LKPP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/ce588ff8-cb49-4708-927e-bfebd18549c4/json/5340/Ecat-PaketEPurchasing/tipe/4:12/parameter/2025:D107`
- Root: list berisi 11733 item

- **Struktur Bidang:**
    ```json
{
        "kd_komoditas": "int",
        "kode_anggaran": "str",
        "nama_paket": "str",
        "ppk_nip": "str",
        "kd_provinsi_wilayah_harga": "int",
        "no_telp_user_pokja": "str",
        "kd_user_ppk": "int",
        "ongkos_kirim": "float",
        "kd_klpd": "str",
        "kuantitas": "float",
        "kd_rup": "int",
        "alamat_satker": "str",
        "jml_jenis_produk": "int",
        "kd_kabupaten_wilayah_harga": "int",
        "kd_produk": "int",
        "kd_user_pokja": "int",
        "nama_sumber_dana": "str",
        "harga_satuan": "float",
        "catatan_produk": "str",
        "email_user_pokja": "str",
        "npwp_satker": "str",
        "kd_paket": "int",
        "tanggal_buat_paket": "str",
        "total_harga": "float",
        "tanggal_edit_paket": "str",
        "paket_status_str": "str",
        "deskripsi": "null",
        "no_paket": "str",
        "status_paket": "str",
        "jabatan_ppk": "str",
        "nama_satker": "null",
        "tahun_anggaran": "int",
        "satker_id": "int",
        "kd_penyedia": "int",
        "kd_penyedia_distributor": "int"
    }
    ```

## 5. [1062] Ecat-PaketEPurchasing-Lama

- Kelompok: PURCHASING
- Deskripsi: Informasi Transaksi e-Purchasing s.d Tahun 2021 (31 Oktober 2021)
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/ccc6bd76-f0d4-4374-a57b-10edfdf20615/json/5366/Ecat-PaketEPurchasing-Lama/tipe/12:4/parameter/D107:2025`
- Status: Gagal memuat data (File JSON kosong)

## 6. [1023] Ecat-PenyediaDetail

- Kelompok: PURCHASING
- Deskripsi: Detail Dari Penyedia berdasarkan Layanan Paket Epurchasing
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/59c70a26-d885-45d9-a199-c2d582361652/json/5338/Ecat-PenyediaDetail/tipe/4/parameter/439515`
- Root: list berisi 1 item

- **Struktur Bidang:**
    ```json
{
        "alamat_penyedia": "str",
        "nama_penyedia": "str",
        "npwp_penyedia": "str",
        "kode_penyedia_sikap": "int",
        "kbli2020_penyedia": "null",
        "npwp_16": "null",
        "penyedia_ukm": "str",
        "email_penyedia": "str",
        "kd_penyedia": "int",
        "no_telp_penyedia": "str"
    }
    ```

## 7. [1024] Ecat-PenyediaDistributorDetail

- Kelompok: PURCHASING
- Deskripsi: Detail Dari Penyedia Distribusi berdasarkan Layanan Paket Epurchasing
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/ba29334b-018e-46af-9b37-df3cc804a573/json/5337/Ecat-PenyediaDistributorDetail/tipe/12/parameter/497198`
- Root: list berisi 1 item

- **Struktur Bidang:**
    ```json
{
        "no_telp_distributor": "str",
        "npwp_distributor": "str",
        "alamat_distributor": "str",
        "nama_distributor": "str",
        "kd_penyedia_distributor": "int",
        "email_distributor": "str"
    }
    ```

## 8. [1022] Ecat-ProdukDetail

- Kelompok: PURCHASING
- Deskripsi: Detail Dari Produk berdasarkan Layanan Paket Epurchasing
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/a76a5bb2-03dc-4898-9730-344d150643c5/json/5360/Ecat-ProdukDetail/tipe/4/parameter/1556172`
- Root: list berisi 1 item

- **Struktur Bidang:**
    ```json
{
        "nie_negara_pabrik": "null",
        "tglkontrak_selesai": "null",
        "nie_id": "null",
        "nie_nama_pabrik": "null",
        "nilai_bmp": "str",
        "nama_sub_kategori_2": "null",
        "nie_kategori": "null",
        "nama_manufaktur": "str",
        "nama_kategori_terkecil": "str",
        "no_produk": "str",
        "nie_hscode": "null",
        "nie_kelas": "null",
        "nama_sub_kategori_4": "null",
        "nie_klasifikasi_izin": "null",
        "masa_berlaku_kontrak": "str",
        "nomor_tkdn": "str",
        "nie_nama_usaha": "null",
        "nie_kemasan": "null",
        "nie_kelas_resiko": "null",
        "no_suket_alkes": "null",
        "nie_ukuran": "null",
        "status_tayang": "str",
        "nama_komoditas": "str",
        "nie": "null",
        "nama_penyedia": "str",
        "kd_produk": "int",
        "nama_sub_kategori_1": "str",
        "kbki_id": "str",
        "tglkontrak_mulai": "str",
        "nie_nib": "null",
        "nie_tgl_terbit": "null",
        "jenis_produk": "str",
        "nie_alamat_pabrik": "null",
        "status": "str",
        "active": "int",
        "apakah_dapat_dibeli": "str",
        "nama_produk": "str",
        "nama_sub_kategori_3": "null",
        "nie_nama_produk": "null",
        "tkdn_produk": "str",
        "berlaku_sampai": "str",
        "created_date": "str",
        "no_kontrak": "str",
        "nie_tgl_expire": "null",
        "modified_date": "str",
        "nie_last_update": "null",
        "nama_pemilik_sertifikat_tkdn": "str",
        "nie_npwp": "null",
        "unit_pengukuran": "str",
        "nie_sub_kategori": "null",
        "nie_jenis_produk": "null",
        "setuju_tolak_tanggal": "str",
        "no_produk_penyedia": "str",
        "kd_produk_kategori": "int",
        "jumlah_stok": "float",
        "harga": "str"
    }
    ```

## 9. [1026] Ecat-UserPegawai

- Kelompok: PURCHASING
- Deskripsi: Detail Dari User Pegawai berdasarkan Layanan Paket Epurchasing
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/a9e75ce8-75a5-441c-9cbe-338c2ac71552/json/5341/Ecat-UserPegawai/tipe/12/parameter/47114582`
- Root: list berisi 1 item

- **Struktur Bidang:**
    ```json
{
        "kd_satker": "int",
        "kd_user_pegawai": "int",
        "jabatan_pegawai": "str",
        "kd_klpd": "str",
        "nama_lengkap": "str",
        "nip_pegawai": "str"
    }
    ```

## 10. [1116] Ecat-MasterKabKota

- Kelompok: PURCHASING
- Deskripsi: Master Kabupaten dan Kota yang ada di App SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/110dbba5-93b1-4d22-bf22-efe75c18a08d/json/8278/Ecat-MasterKabKota/tipe/12/parameter/MasterKabKota`
- Root: list berisi 514 item

- **Struktur Bidang:**
    ```json
{
        "kd_provinsi": "int",
        "kd_kabupaten": "int",
        "nama_kabupaten": "str"
    }
    ```

## 11. [1117] Ecat-MasterProvinsi

- Kelompok: PURCHASING
- Deskripsi: Master Provinsi yang ada di App SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/de6b4b40-302f-4d50-bf75-965d4f920763/json/8404/Ecat-MasterProvinsi/tipe/12/parameter/MasterProvinsi`
- Root: list berisi 38 item

- **Struktur Bidang:**
    ```json
{
        "kd_provinsi": "int",
        "nama_provinsi": "str"
    }
    ```

## 12. [1040] RUP-KegiatanMaster

- Kelompok: SIRUP
- Deskripsi: Data Kegiatan RUP Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/7201cbd3-6a84-44dc-ada7-96c8bdaad80e/json/5344/RUP-KegiatanMaster/tipe/4:12/parameter/2025:D107`
- Root: list berisi 1150 item

- **Struktur Bidang:**
    ```json
{
        "jenis_klpd": "str",
        "kd_satker": "int",
        "nama_kegiatan": "str",
        "kd_kegiatan_lokal": "null",
        "kd_kegiatan_str": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "kd_klpd": "str",
        "kd_kegiatan": "int",
        "pagu_kegiatan": "int",
        "is_deleted": "bool",
        "tahun_anggaran": "int",
        "kd_program": "int"
    }
    ```

## 13. [1035] RUP-KomponenMaster

- Kelompok: SIRUP
- Deskripsi: Data Komponen RUP Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/dd1b4d14-1ca2-468f-ae7c-39945895e3dc/json/5345/RUP-KomponenMaster/tipe/4:12/parameter/2025:D107`
- Status: Gagal memuat data (File JSON kosong)

## 14. [1037] RUP-KROMaster

- Kelompok: SIRUP
- Deskripsi: Data Klasifikasi Rincian Output RUP Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/f831c813-20a3-4da8-88c7-b847e9bffe59/json/5342/RUP-KROMaster/tipe/4:12/parameter/2025:D107`
- Status: Gagal memuat data (File JSON kosong)

## 15. [1065] RUP-MasterKabKota

- Kelompok: SIRUP
- Deskripsi: Master Kabupaten dan Kota yang ada di App SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/d29437be-a776-4bea-a04c-f9618172609f/json/5367/RUP-MasterKabKota/tipe/12/parameter/RUP-MasterKabKota`
- Root: list berisi 519 item

- **Struktur Bidang:**
    ```json
{
        "kd_provinsi": "int",
        "nama_kabkota": "str",
        "kd_kabkota": "int"
    }
    ```

## 16. [1066] RUP-MasterProvinsi

- Kelompok: SIRUP
- Deskripsi: Master Provinsi yang ada di App SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/3bb79b43-6bef-4b72-ab3c-462374dac67d/json/5368/RUP-MasterProvinsi/tipe/12/parameter/RUP-MasterProvinsi`
- Root: list berisi 38 item

- **Struktur Bidang:**
    ```json
{
        "kd_provinsi": "int",
        "nama_provinsi": "str"
    }
    ```

## 17. [1008] RUP-MasterSatker

- Kelompok: SIRUP
- Deskripsi: MasterSatker dari Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/0bebaf75-7ade-41f8-bc9b-57ab63c99e82/json/5356/RUP-MasterSatker/tipe/12:12/parameter/D107:2025`
- Root: list berisi 165 item

- **Struktur Bidang:**
    ```json
{
        "kd_satker": "int",
        "jenis_klpd": "str",
        "status_satker": "str",
        "kd_satker_str": "str",
        "jenis_satker": "str",
        "telepon": "null",
        "kd_klpd": "str",
        "nama_klpd": "str",
        "fax": "null",
        "alamat": "null",
        "nama_satker": "str",
        "ket_satker": "str",
        "kode_eselon": "null",
        "kodepos": "null"
    }
    ```

## 18. [1028] RUP-PaketAnggaranPenyedia

- Kelompok: SIRUP
- Deskripsi: Data Transaksional RUP Paket Anggaran Penyedia Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/a89d14ba-112d-4b15-b157-4462141735ac/json/5355/RUP-PaketAnggaranPenyedia/tipe/4:12/parameter/2025:D107`
- Root: list berisi 17115 item

- **Struktur Bidang:**
    ```json
{
        "sumber_dana": "str",
        "kd_subkegiatan": "int",
        "tahun_anggaran_dana": "int",
        "status_umumkan_rup": "str",
        "kd_satker": "int",
        "kd_klpd": "str",
        "kd_kegiatan": "int",
        "asal_dana": "str",
        "kd_rup": "int",
        "status_delete_rup": "bool",
        "mak": "str",
        "kd_satker_str": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "asal_dana_satker": "str",
        "kd_komponen": "null",
        "status_aktif_rup": "bool",
        "pagu": "int",
        "jenis_klpd": "str",
        "asal_dana_klpd": "str",
        "kd_rup_lokal": "null",
        "nama_satker": "str",
        "tahun_anggaran": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `kd_kegiatan` memiliki beberapa tipe: `int, null`

## 19. [1033] RUP-PaketAnggaranSwakelola

- Kelompok: SIRUP
- Deskripsi: Data Transaksional RUP Paket Anggaran Swakelola Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/52e3526e-963f-404c-9ade-b51fa3cab728/json/5373/RUP-PaketAnggaranSwakelola/tipe/4:12/parameter/2025:D107`
- Root: list berisi 16957 item

- **Struktur Bidang:**
    ```json
{
        "sumber_dana": "str",
        "kd_subkegiatan": "int",
        "tahun_anggaran_dana": "int",
        "status_umumkan_rup": "str",
        "kd_satker": "int",
        "kd_klpd": "str",
        "kd_kegiatan": "int",
        "asal_dana": "str",
        "kd_rup": "int",
        "status_delete_rup": "bool",
        "mak": "str",
        "kd_satker_str": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "asal_dana_satker": "str",
        "kd_komponen": "null",
        "status_aktif_rup": "bool",
        "pagu": "int",
        "jenis_klpd": "str",
        "asal_dana_klpd": "str",
        "kd_rup_lokal": "null",
        "nama_satker": "str",
        "tahun_anggaran": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `kd_subkegiatan` memiliki beberapa tipe: `int, null`
  - Field `kd_kegiatan` memiliki beberapa tipe: `int, null`

## 20. [1029] RUP-PaketPenyediaLokasi

- Kelompok: SIRUP
- Deskripsi: Data Transaksional RUP Paket Penyedia Lokasi Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/314f2e60-7173-4395-812b-c9ff4eadc319/json/5358/RUP-PaketPenyediaLokasi/tipe/4:12/parameter/2025:D107`
- Root: list berisi 20889 item

- **Struktur Bidang:**
    ```json
{
        "jenis_klpd": "str",
        "kd_satker": "int",
        "kd_provinsi": "int",
        "kd_satker_str": "str",
        "kab_kota": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "kd_klpd": "str",
        "kd_kab_kota": "int",
        "detail_lokasi": "str",
        "kd_rup": "int",
        "nama_satker": "str",
        "tahun_anggaran": "int",
        "provinsi": "str"
    }
    ```

## 21. [1018] RUP-PaketPenyedia-Terumumkan

- Kelompok: SIRUP
- Deskripsi: Data Transaksional RUP Paket Penyedia Terumumkan Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/b3bd3bfd-a027-4dbb-b7e4-883bfc5eac37/json/5352/RUP-PaketPenyedia-Terumumkan/tipe/4:12/parameter/2025:D107`
- Root: list berisi 12013 item

- **Struktur Bidang:**
    ```json
{
        "spp_aspek_lingkungan": "bool",
        "status_pdn": "str",
        "nama_paket": "str",
        "tgl_awal_pemilihan": "str",
        "tipe_paket": "str",
        "tgl_akhir_pemanfaatan": "str",
        "tgl_awal_pemanfaatan": "str",
        "tgl_akhir_kontrak": "str",
        "status_umumkan_rup": "str",
        "kode_rup_tahun_pertama": "null",
        "nomor_kontrak": "null",
        "kd_satker": "int",
        "status_dikecualikan": "bool",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "volume_pekerjaan": "str",
        "status_delete_rup": "bool",
        "kd_rup": "int",
        "kd_metode_pengadaan": "int",
        "status_ukm": "str",
        "jenis_pengadaan": "str",
        "kd_jenis_pengadaan": "str",
        "spp_aspek_ekonomi": "bool",
        "kd_satker_str": "str",
        "status_konsolidasi": "str",
        "spesifikasi_pekerjaan": "str",
        "username_ppk": "str",
        "tgl_pengumuman_paket": "str",
        "alasan_non_ukm": "null",
        "nama_klpd": "str",
        "urarian_pekerjaan": "str",
        "tgl_buat_paket": "str",
        "_event_date": "str",
        "alasan_dikecualikan": "null",
        "tahun_pertama": "null",
        "spp_aspek_sosial": "bool",
        "status_aktif_rup": "bool",
        "pagu": "int",
        "tgl_akhir_pemilihan": "str",
        "jenis_klpd": "str",
        "metode_pengadaan": "str",
        "kd_rup_lokal": "null",
        "nama_satker": "str",
        "kd_rup_swakelola": "null",
        "tahun_anggaran": "int",
        "nama_ppk": "str",
        "tgl_awal_kontrak": "str",
        "status_pradipa": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `nip_ppk` memiliki beberapa tipe: `null, str`
  - Field `username_ppk` memiliki beberapa tipe: `null, str`
  - Field `alasan_non_ukm` memiliki beberapa tipe: `null, str`
  - Field `alasan_dikecualikan` memiliki beberapa tipe: `null, str`
  - Field `kd_rup_swakelola` memiliki beberapa tipe: `int, null`
  - Field `nama_ppk` memiliki beberapa tipe: `null, str`

## 22. [1032] RUP-PaketSwakelolaLokasi

- Kelompok: SIRUP
- Deskripsi: Data Transaksional RUP Paket Swakelola Lokasi Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/40fe2856-56ee-4179-81fc-3ba339668b60/json/5359/RUP-PaketSwakelolaLokasi/tipe/4:12/parameter/2025:D107`
- Root: list berisi 10580 item

- **Struktur Bidang:**
    ```json
{
        "jenis_klpd": "str",
        "kd_satker": "int",
        "kd_provinsi": "int",
        "kd_satker_str": "str",
        "kab_kota": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "kd_klpd": "str",
        "kd_kab_kota": "int",
        "detail_lokasi": "str",
        "kd_rup": "int",
        "nama_satker": "str",
        "tahun_anggaran": "int",
        "provinsi": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `kd_provinsi` memiliki beberapa tipe: `int, null`
  - Field `kab_kota` memiliki beberapa tipe: `null, str`
  - Field `kd_kab_kota` memiliki beberapa tipe: `int, null`
  - Field `detail_lokasi` memiliki beberapa tipe: `null, str`
  - Field `provinsi` memiliki beberapa tipe: `null, str`

## 23. [1030] RUP-PaketSwakelola-Terumumkan

- Kelompok: SIRUP
- Deskripsi: Data Transaksional RUP Paket Swakelola Terumumkan Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/50b279ec-7d75-4f0d-b5e1-73d9f5037810/json/5353/RUP-PaketSwakelola-Terumumkan/tipe/4:12/parameter/2025:D107`
- Root: list berisi 5555 item

- **Struktur Bidang:**
    ```json
{
        "nama_paket": "str",
        "status_umumkan_rup": "str",
        "kd_satker": "int",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "volume_pekerjaan": "str",
        "status_delete_rup": "bool",
        "kd_rup": "int",
        "tipe_swakelola": "int",
        "kd_satker_str": "str",
        "kd_klpd_penyelenggara": "null",
        "tgl_akhir_pelaksanaan_kontrak": "str",
        "username_ppk": "str",
        "tgl_pengumuman_paket": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "nama_satker_penyelenggara": "null",
        "tgl_buat_paket": "str",
        "status_aktif_rup": "bool",
        "pagu": "int",
        "uraian_pekerjaan": "str",
        "jenis_klpd": "str",
        "nama_klpd_penyelenggara": "null",
        "kd_rup_lokal": "null",
        "tgl_awal_pelaksanaan_kontrak": "str",
        "nama_satker": "str",
        "nama_ppk": "str",
        "tahun_anggaran": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `nip_ppk` memiliki beberapa tipe: `null, str`
  - Field `kd_klpd_penyelenggara` memiliki beberapa tipe: `null, str`
  - Field `nama_satker_penyelenggara` memiliki beberapa tipe: `null, str`
  - Field `nama_klpd_penyelenggara` memiliki beberapa tipe: `null, str`
  - Field `nama_ppk` memiliki beberapa tipe: `null, str`

## 24. [1041] RUP-ProgramMaster

- Kelompok: SIRUP
- Deskripsi: Data Program RUP Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/968d73cb-bbb5-4aa1-8ae9-1cf2e0b03044/json/5354/RUP-ProgramMaster/tipe/4:12/parameter/2025:D107`
- Root: list berisi 409 item

- **Struktur Bidang:**
    ```json
{
        "jenis_klpd": "str",
        "kd_satker": "int",
        "kd_program_lokal": "null",
        "pagu_program": "int",
        "nama_klpd": "str",
        "kd_klpd": "str",
        "_event_date": "str",
        "is_deleted": "bool",
        "tahun_anggaran": "int",
        "nama_program": "str",
        "kd_program_str": "str",
        "kd_program": "int"
    }
    ```

## 25. [1038] RUP-ROMaster

- Kelompok: SIRUP
- Deskripsi: Data Rincian Output RUP Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/de6ab80c-4234-453b-90a2-e62ca3f10793/json/5357/RUP-ROMaster/tipe/4:12/parameter/2025:D107`
- Status: Gagal memuat data (File JSON kosong)

## 26. [1067] RUP-StrukturAnggaranKL

- Kelompok: SIRUP
- Deskripsi: Layanan Struktur Anggaran KL yang sudah disesuaikan dengan Perpres 12/2021
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/67681ee6-3893-4909-8449-3ad19043b4cf/json/5369/RUP-StrukturAnggaranKL/tipe/4:12/parameter/2025:D107`
- Status: Gagal memuat data (File JSON kosong)

## 27. [1084] RUP-StrukturAnggaranPD

- Kelompok: SIRUP
- Deskripsi: Layanan Struktur Anggaran PD yang sudah disesuaikan dengan Perpres 12/2021
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/a1e5b4aa-4777-4aa3-812d-6e65657b7edd/json/7024/RUP-StrukturAnggaranPD/tipe/4:12/parameter/2025:D107`
- Root: list berisi 165 item

- **Struktur Bidang:**
    ```json
{
        "kd_satker": "int",
        "total_belanja": "int",
        "kd_satker_str": "str",
        "belanja_btt": "int",
        "nama_klpd": "str",
        "kd_klpd": "str",
        "belanja_modal": "int",
        "belanja_non_pengadaan": "int",
        "belanja_operasi": "int",
        "nama_satker": "str",
        "belanja_pengadaan": "int",
        "tahun_anggaran": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `total_belanja` memiliki beberapa tipe: `int, null`
  - Field `belanja_btt` memiliki beberapa tipe: `int, null`
  - Field `belanja_modal` memiliki beberapa tipe: `int, null`
  - Field `belanja_non_pengadaan` memiliki beberapa tipe: `int, null`
  - Field `belanja_operasi` memiliki beberapa tipe: `int, null`
  - Field `belanja_pengadaan` memiliki beberapa tipe: `int, null`
  - Field `tahun_anggaran` memiliki beberapa tipe: `int, null`

## 28. [1039] RUP-SubKegiatanMaster

- Kelompok: SIRUP
- Deskripsi: Data Sub Kegiatan RUP Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/d232ce75-7090-450c-865a-da5ecfcb92b0/json/5336/RUP-SubKegiatanMaster/tipe/4:12/parameter/2025:D107`
- Root: list berisi 3949 item

- **Struktur Bidang:**
    ```json
{
        "jenis_klpd": "str",
        "kd_satker": "int",
        "kd_subkegiatan_str": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "kd_klpd": "str",
        "nama_subkegiatan": "str",
        "kd_kegiatan": "int",
        "kd_subkegiatan": "int",
        "pagu_subkegiatan": "int",
        "kd_subkegiatan_lokal": "null",
        "is_deleted": "bool",
        "tahun_anggaran": "int",
        "kd_program": "int"
    }
    ```

## 29. [1036] RUP-SubKomponenMaster

- Kelompok: SIRUP
- Deskripsi: Data Sub Komponen RUP Sesuai dengan Aplikasi SiRUP
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/20691094-8e05-4a23-a4db-910ab47e656a/json/5372/RUP-SubKomponenMaster/tipe/4:12/parameter/2025:D107`
- Status: Gagal memuat data (File JSON kosong)

## 30. [1069] SPSE-JadwalTahapanNonTender

- Kelompok: SPSE
- Deskripsi: Layanan Jadwal Tahapan Non Tender pada Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/64d7d20e-9cf4-4944-ae72-c3e2f9ad3782/json/5371/SPSE-JadwalTahapanNonTender/tipe/4:4/parameter/2025:93`
- Root: list berisi 11930 item

- **Struktur Bidang:**
    ```json
{
        "kd_satker": "str",
        "tgl_akhir": "str",
        "kd_satker_str": "str",
        "kd_akt": "int",
        "_event_date": "str",
        "kd_klpd": "str",
        "tgl_awal": "str",
        "nama_akt": "str",
        "kd_tahapan": "int",
        "kd_nontender": "int",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "nama_tahapan": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `tgl_akhir` memiliki beberapa tipe: `null, str`
  - Field `tgl_awal` memiliki beberapa tipe: `null, str`
  - Field `nama_tahapan` memiliki beberapa tipe: `null, str`

## 31. [1068] SPSE-JadwalTahapanTender

- Kelompok: SPSE
- Deskripsi: Layanan Jadwal Tahapan Tender pada Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/ebaadb68-54af-4641-a677-9d06d21461d9/json/5370/SPSE-JadwalTahapanTender/tipe/4:4/parameter/2025:93`
- Root: list berisi 1428 item

- **Struktur Bidang:**
    ```json
{
        "kd_satker": "str",
        "tgl_akhir": "str",
        "kd_satker_str": "str",
        "kd_tender": "int",
        "kd_akt": "int",
        "_event_date": "str",
        "kd_klpd": "str",
        "tgl_awal": "str",
        "nama_akt": "null",
        "kd_tahapan": "int",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "nama_tahapan": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `nama_tahapan` memiliki beberapa tipe: `null, str`

## 32. [1082] SPSE-NonTenderEkontrak-4BAPBAST

- Kelompok: SPSE
- Deskripsi: Data Non Tender EKontrak yang sudah menginputkan BAP BAST oleh PPK pada SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/86383278-9b87-4f62-8dd4-ef9776e64d6c/json/6805/SPSE-NonTenderEkontrak-BAPBAST/tipe/4:4/parameter/2025:93`
- Root: list berisi 863 item

- **Struktur Bidang:**
    ```json
{
        "progres_pekerjaan": "int",
        "tgl_bast": "str",
        "tgl_penetapan_status_kontrak": "str",
        "nama_paket": "str",
        "kd_nontender": "int",
        "no_bast": "str",
        "kd_satker": "str",
        "wakil_sah_penyedia": "null",
        "mtd_pengadaan": "str",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "cara_pembayaran_kontrak": "str",
        "versi_addendum": "int",
        "jabatan_wakil_penyedia": "str",
        "kd_lpse": "int",
        "besar_pembayaran": "int",
        "alamat_satker": "str",
        "jabatan_penandatangan_sk": "str",
        "status_kontrak": "str",
        "alasan_addendum": "null",
        "_inserted_date": "str",
        "no_bap": "str",
        "nama_penyedia": "str",
        "alamat_penyedia": "str",
        "kd_satker_str": "str",
        "npwp_penyedia": "str",
        "tgl_bap": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "alasan_penetapan_status_kontrak": "null",
        "jenis_klpd": "str",
        "lingkup_pekerjaan": "null",
        "no_kontrak": "str",
        "npwp_16_penyedia": "str",
        "jabatan_ppk": "str",
        "nama_satker": "str",
        "nama_ppk": "str",
        "tahun_anggaran": "int",
        "nilai_kontrak": "int",
        "no_sk_ppk": "str",
        "no_sppbj": "str",
        "tgl_kontrak": "str",
        "apakah_addendum": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `progres_pekerjaan` memiliki beberapa tipe: `float, int, null`
  - Field `tgl_bast` memiliki beberapa tipe: `null, str`
  - Field `tgl_penetapan_status_kontrak` memiliki beberapa tipe: `null, str`
  - Field `cara_pembayaran_kontrak` memiliki beberapa tipe: `null, str`
  - Field `besar_pembayaran` memiliki beberapa tipe: `float, int`
  - Field `_inserted_date` memiliki beberapa tipe: `null, str`
  - Field `npwp_16_penyedia` memiliki beberapa tipe: `null, str`
  - Field `nilai_kontrak` memiliki beberapa tipe: `float, int`

## 33. [1080] SPSE-NonTenderEkontrak-2Kontrak

- Kelompok: SPSE
- Deskripsi: Data Non Tender EKontrak yang sudah menginputkan Kontrak oleh PPK pada SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/ce352fab-3e39-4583-b04f-af22c986d548/json/6589/SPSE-NonTenderEkontrak-Kontrak/tipe/4:4/parameter/2025:93`
- Root: list berisi 1047 item

- **Struktur Bidang:**
    ```json
{
        "alasan_nilai_kontrak_10_persen": "null",
        "tgl_penetapan_status_kontrak": "str",
        "nama_paket": "str",
        "kd_nontender": "int",
        "bentuk_usaha_penyedia": "str",
        "kd_satker": "str",
        "wakil_sah_penyedia": "str",
        "nilai_umk_kontrak": "int",
        "mtd_pengadaan": "str",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "versi_addendum": "int",
        "apakah_addendum": "str",
        "jabatan_wakil_penyedia": "str",
        "kota_kontrak": "str",
        "tgl_kontrak_akhir": "null",
        "alamat_satker": "str",
        "status_kontrak": "str",
        "alasan_addendum": "null",
        "nama_penyedia": "str",
        "npwp_penyedia": "str",
        "kd_satker_str": "str",
        "nama_klpd": "str",
        "nama_pemilik_rek_bank": "null",
        "anggota_kso": "null",
        "jenis_kontrak": "str",
        "no_rek_bank": "str",
        "nilai_kontrak": "int",
        "tgl_kontrak_awal": "null",
        "nilai_pdn_kontrak": "int",
        "alasan_penetapan_status_kontrak": "null",
        "nama_rek_bank": "str",
        "jenis_klpd": "str",
        "lingkup_pekerjaan": "null",
        "no_kontrak": "str",
        "npwp16_penyedia": "str",
        "alasan_ubah_nilai_kontrak": "str",
        "informasi_lainnya": "null",
        "jabatan_ppk": "str",
        "nama_satker": "str",
        "nama_ppk": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "no_sk_ppk": "str",
        "no_sppbj": "str",
        "tgl_kontrak": "str",
        "tipe_penyedia": "null"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `tgl_penetapan_status_kontrak` memiliki beberapa tipe: `null, str`
  - Field `bentuk_usaha_penyedia` memiliki beberapa tipe: `null, str`
  - Field `wakil_sah_penyedia` memiliki beberapa tipe: `null, str`
  - Field `nilai_umk_kontrak` memiliki beberapa tipe: `float, int`
  - Field `jabatan_wakil_penyedia` memiliki beberapa tipe: `null, str`
  - Field `tgl_kontrak_akhir` memiliki beberapa tipe: `null, str`
  - Field `alasan_addendum` memiliki beberapa tipe: `null, str`
  - Field `nama_penyedia` memiliki beberapa tipe: `null, str`
  - Field `npwp_penyedia` memiliki beberapa tipe: `null, str`
  - Field `nama_pemilik_rek_bank` memiliki beberapa tipe: `null, str`
  - Field `nilai_kontrak` memiliki beberapa tipe: `float, int`
  - Field `tgl_kontrak_awal` memiliki beberapa tipe: `null, str`
  - Field `nilai_pdn_kontrak` memiliki beberapa tipe: `float, int`
  - Field `lingkup_pekerjaan` memiliki beberapa tipe: `null, str`
  - Field `npwp16_penyedia` memiliki beberapa tipe: `null, str`
  - Field `informasi_lainnya` memiliki beberapa tipe: `null, str`
  - Field `tipe_penyedia` memiliki beberapa tipe: `null, str`

## 34. [1083] SPSE-NonTenderEkontrak-3SPMKSPP

- Kelompok: SPSE
- Deskripsi: Data Non Tender EKontrak yang sudah menginputkan SPMK SPP oleh PPK pada SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/c0cd83b0-a4f3-4d43-8b9d-27aa6a33d4fa/json/6913/SPSE-NonTenderEkontrak-SPMKSPP/tipe/4:4/parameter/2025:93`
- Root: list berisi 965 item

- **Struktur Bidang:**
    ```json
{
        "tgl_penetapan_status_kontrak": "null",
        "nama_paket": "str",
        "tgl_selesai_pekerjaan": "str",
        "kota_spmk_spp": "str",
        "kd_nontender": "int",
        "kd_satker": "str",
        "wakil_sah_penyedia": "str",
        "mtd_pengadaan": "str",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "versi_addendum": "int",
        "jabatan_wakil_penyedia": "str",
        "no_spmk_spp": "str",
        "waktu_penyelesaian": "str",
        "alamat_satker": "str",
        "tgl_mulai_pekerjaan": "str",
        "status_kontrak": "str",
        "alasan_addendum": "null",
        "nama_penyedia": "str",
        "alamat_penyedia": "str",
        "kd_satker_str": "str",
        "npwp_penyedia": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "alamat_pengiriman": "null",
        "tgl_spmk_spp": "str",
        "alasan_penetapan_status_kontrak": "null",
        "jenis_klpd": "str",
        "no_kontrak": "str",
        "npwp_16_penyedia": "str",
        "jabatan_ppk": "str",
        "nama_satker": "str",
        "nama_ppk": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "no_sppbj": "str",
        "tgl_kontrak": "str",
        "apakah_addendum": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `tgl_penetapan_status_kontrak` memiliki beberapa tipe: `null, str`
  - Field `alasan_addendum` memiliki beberapa tipe: `null, str`
  - Field `alamat_pengiriman` memiliki beberapa tipe: `null, str`
  - Field `npwp_16_penyedia` memiliki beberapa tipe: `null, str`

## 35. [1081] SPSE-NonTenderEkontrak-1SPPBJ

- Kelompok: SPSE
- Deskripsi: Data Non Tender EKontrak yang sudah menginputkan SPPBJ oleh PPK pada SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/816bf38a-c1f6-4811-af32-bb34e7bbeed0/json/6697/SPSE-NonTenderEkontrak-SPPBJ/tipe/4:4/parameter/2025:93`
- Root: list berisi 1302 item

- **Struktur Bidang:**
    ```json
{
        "lampiran_sppbj": "str",
        "tgl_penetapan_status_kontrak": "null",
        "nama_paket": "str",
        "kd_nontender": "int",
        "harga_final": "int",
        "kd_satker": "str",
        "nilai_jaminan_pelaksanaan": "int",
        "mtd_pengadaan": "str",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "versi_addendum": "int",
        "tgl_sppbj": "str",
        "alamat_satker": "str",
        "kota_sppbj": "str",
        "status_kontrak": "str",
        "alasan_addendum": "null",
        "masa_berlaku_jaminan": "int",
        "nama_penyedia": "str",
        "npwp_penyedia": "str",
        "kd_satker_str": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "alasan_penetapan_status_kontrak": "null",
        "jenis_klpd": "str",
        "npwp_penyedia_16": "str",
        "jabatan_ppk": "str",
        "nama_satker": "str",
        "nama_ppk": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "no_sppbj": "str",
        "apakah_addendum": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `tgl_penetapan_status_kontrak` memiliki beberapa tipe: `null, str`
  - Field `harga_final` memiliki beberapa tipe: `float, int`
  - Field `nilai_jaminan_pelaksanaan` memiliki beberapa tipe: `float, int`
  - Field `nip_ppk` memiliki beberapa tipe: `null, str`
  - Field `alasan_addendum` memiliki beberapa tipe: `null, str`
  - Field `masa_berlaku_jaminan` memiliki beberapa tipe: `int, null`
  - Field `npwp_penyedia_16` memiliki beberapa tipe: `null, str`
  - Field `nama_ppk` memiliki beberapa tipe: `null, str`

## 36. [1016] SPSE-NonTenderPengumuman

- Kelompok: SPSE
- Deskripsi: Layanan Non Tender Pengumuman dari Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/0c1aafcf-1a42-4347-9611-0c7db5e60860/json/5346/SPSE-NonTenderPengumuman/tipe/4:4/parameter/2025:93`
- Root: list berisi 2386 item

- **Struktur Bidang:**
    ```json
{
        "repeat_order": "str",
        "sumber_dana": "str",
        "ket_diulang": "null",
        "nama_paket": "str",
        "kd_nontender": "int",
        "kd_satker": "str",
        "nama_lpse": "str",
        "mtd_pemilihan": "str",
        "kd_klpd": "str",
        "hps": "int",
        "kontrak_pembayaran": "str",
        "url_lpse": "str",
        "kd_rup": "str",
        "tgl_kolektif_kolegial": "str",
        "mak": "str",
        "tgl_pengumuman_nontender": "str",
        "jenis_pengadaan": "str",
        "nip_nama_ppk": "str",
        "kd_satker_str": "str",
        "status_nontender": "str",
        "nama_klpd": "str",
        "ket_ditutup": "null",
        "tgl_buat_paket": "str",
        "kualifikasi_paket": "str",
        "pagu": "int",
        "nip_nama_pp": "str",
        "jenis_klpd": "str",
        "kd_pkt_dce": "int",
        "lls_id": "int",
        "nip_nama_pokja": "null",
        "versi_nontender": "int",
        "nama_satker": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `hps` memiliki beberapa tipe: `float, int`
  - Field `tgl_pengumuman_nontender` memiliki beberapa tipe: `null, str`
  - Field `nip_nama_ppk` memiliki beberapa tipe: `null, str`
  - Field `ket_ditutup` memiliki beberapa tipe: `null, str`
  - Field `nip_nama_pp` memiliki beberapa tipe: `null, str`
  - Field `nip_nama_pokja` memiliki beberapa tipe: `null, str`

## 37. [1017] SPSE-NonTenderSelesai

- Kelompok: SPSE
- Deskripsi: Layanan Non Tender Selesai dari Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/fbc46882-a3b5-444b-b0c8-4dfe7856e73c/json/5349/SPSE-NonTenderSelesai/tipe/4:4/parameter/2025:93`
- Root: list berisi 1868 item

- **Struktur Bidang:**
    ```json
{
        "lpse_id": "int",
        "sumber_dana": "str",
        "nama_paket": "str",
        "kd_nontender": "int",
        "kd_satker": "str",
        "nilai_negosiasi": "int",
        "nama_lpse": "str",
        "nilai_umk_kontrak": "int",
        "mtd_pemilihan": "str",
        "kd_klpd": "str",
        "hps": "int",
        "kontrak_pembayaran": "str",
        "url_lpse": "str",
        "kd_rup": "str",
        "tgl_pengumuman_nontender": "str",
        "mak": "str",
        "tgl_penarikan": "str",
        "jenis_pengadaan": "str",
        "nama_penyedia": "str",
        "npwp_penyedia": "str",
        "kd_satker_str": "str",
        "tgl_selesai_nontender": "str",
        "status_nontender": "str",
        "nama_klpd": "str",
        "nilai_terkoreksi": "int",
        "nilai_kontrak": "int",
        "kualifikasi_paket": "str",
        "pagu": "int",
        "nilai_pdn_kontrak": "int",
        "jenis_klpd": "str",
        "kd_pkt_dce": "int",
        "nilai_penawaran": "int",
        "npwp16_penyedia": "str",
        "nama_satker": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "kd_penyedia": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `nilai_negosiasi` memiliki beberapa tipe: `float, int, null`
  - Field `nilai_umk_kontrak` memiliki beberapa tipe: `float, int, null`
  - Field `hps` memiliki beberapa tipe: `float, int`
  - Field `nilai_terkoreksi` memiliki beberapa tipe: `float, int, null`
  - Field `nilai_kontrak` memiliki beberapa tipe: `float, int, null`
  - Field `nilai_pdn_kontrak` memiliki beberapa tipe: `float, int, null`
  - Field `nilai_penawaran` memiliki beberapa tipe: `float, int, null`
  - Field `npwp16_penyedia` memiliki beberapa tipe: `null, str`

## 38. [1057] SPSE-PencatatanNonTender

- Kelompok: SPSE
- Deskripsi: Layanan Pencatatan Non Tender dari Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/e01babed-340e-41fb-9bd4-7e4dde5720e9/json/5361/SPSE-PencatatanNonTender/tipe/4:4/parameter/2025:93`
- Root: list berisi 383 item

- **Struktur Bidang:**
    ```json
{
        "sumber_dana": "str",
        "nama_paket": "str",
        "nilai_umk_pct": "int",
        "status_nontender_pct": "str",
        "kd_satker": "str",
        "mtd_pemilihan": "str",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "kd_rup": "str",
        "kd_nontender_pct": "int",
        "kategori_pengadaan": "str",
        "nilai_pdn_pct": "int",
        "kd_satker_str": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "tgl_buat_paket": "str",
        "pagu": "int",
        "uraian_pekerjaan": "str",
        "bukti_pembayaran": "str",
        "alasan_pembatalan": "null",
        "jenis_klpd": "str",
        "kd_pkt_dce": "int",
        "tgl_selesai_paket": "str",
        "informasi_lainnya": "null",
        "nama_satker": "str",
        "total_realisasi": "int",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "nama_ppk": "str",
        "status_nontender_pct_ket": "str",
        "tgl_mulai_paket": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `nilai_umk_pct` memiliki beberapa tipe: `float, int`
  - Field `nilai_pdn_pct` memiliki beberapa tipe: `float, int`
  - Field `alasan_pembatalan` memiliki beberapa tipe: `null, str`
  - Field `total_realisasi` memiliki beberapa tipe: `int, null`

## 39. [1058] SPSE-PencatatanNonTenderRealisasi

- Kelompok: SPSE
- Deskripsi: Layanan Pencatatan Non Tender Realisasi dari Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/e6ba6e46-8880-4040-8794-c807881bee0d/json/5363/SPSE-PencatatanNonTenderRealisasi/tipe/4:4/parameter/2025:93`
- Root: list berisi 485 item

- **Struktur Bidang:**
    ```json
{
        "no_realisasi": "str",
        "nama_paket": "str",
        "kd_rup_paket": "str",
        "kd_satker": "str",
        "nama_lpse": "str",
        "tgl_realisasi": "str",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "kd_nontender_pct": "int",
        "ket_realisasi": "str",
        "dok_realisasi": "null",
        "nama_penyedia": "str",
        "npwp_penyedia": "str",
        "kd_satker_str": "str",
        "jenis_realisasi": "str",
        "nama_klpd": "str",
        "_event_date": "str",
        "pagu": "int",
        "jenis_klpd": "str",
        "kd_paket_dce": "int",
        "nilai_realisasi": "int",
        "nama_satker": "str",
        "nama_ppk": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `dok_realisasi` memiliki beberapa tipe: `null, str`
  - Field `nama_penyedia` memiliki beberapa tipe: `null, str`
  - Field `npwp_penyedia` memiliki beberapa tipe: `null, str`

## 40. [1059] SPSE-PencatatanSwakelola

- Kelompok: SPSE
- Deskripsi: Layanan Pencatatan Swakelola dari Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/e31544e2-ea6a-4f57-b1a6-1014f7a6be1a/json/5364/SPSE-PencatatanSwakelola/tipe/4:4/parameter/2025:93`
- Root: list berisi 209 item

- **Struktur Bidang:**
    ```json
{
        "sumber_dana": "str",
        "nama_paket": "str",
        "status_swakelola_pct_ket": "str",
        "nilai_umk_pct": "int",
        "status_swakelola_pct": "str",
        "kd_satker": "str",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "kd_rup": "str",
        "nilai_pdn_pct": "int",
        "tipe_swakelola": "int",
        "kd_satker_str": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "tipe_swakelola_nama": "str",
        "tgl_buat_paket": "str",
        "pagu": "int",
        "uraian_pekerjaan": "str",
        "alasan_pembatalan": "null",
        "jenis_klpd": "str",
        "kd_pkt_dce": "int",
        "tgl_selesai_paket": "str",
        "informasi_lainnya": "null",
        "kd_swakelola_pct": "int",
        "nama_satker": "str",
        "total_realisasi": "int",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "nama_ppk": "str",
        "tgl_mulai_paket": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `tipe_swakelola` memiliki beberapa tipe: `int, null`
  - Field `tipe_swakelola_nama` memiliki beberapa tipe: `null, str`
  - Field `uraian_pekerjaan` memiliki beberapa tipe: `null, str`
  - Field `alasan_pembatalan` memiliki beberapa tipe: `null, str`
  - Field `total_realisasi` memiliki beberapa tipe: `int, null`

## 41. [1060] SPSE-PencatatanSwakelolaRealisasi

- Kelompok: SPSE
- Deskripsi: Layanan Pencatatan Swakelola Realisasi dari Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/db4aa81b-b62c-49d4-8f13-2287f1fdca9b/json/5365/SPSE-PencatatanSwakelolaRealisasi/tipe/4:4/parameter/2025:93`
- Root: list berisi 432 item

- **Struktur Bidang:**
    ```json
{
        "kd_satker": "str",
        "no_realisasi": "str",
        "tgl_realisasi": "str",
        "jenis_realisasi": "str",
        "_event_date": "str",
        "kd_klpd": "str",
        "nip_ppk": "int",
        "npwp_pelaksana": "str",
        "nilai_realisasi": "int",
        "kd_swakelola_pct": "int",
        "ket_realisasi": "str",
        "nama_ppk": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "nama_pelaksana": "str",
        "dok_realisasi": "null"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `npwp_pelaksana` memiliki beberapa tipe: `null, str`
  - Field `nama_pelaksana` memiliki beberapa tipe: `null, str`
  - Field `dok_realisasi` memiliki beberapa tipe: `null, str`

## 42. [1070] SPSE-PesertaTender

- Kelompok: SPSE
- Deskripsi: Data Peserta Tender dari Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/89ec1f11-74ec-4daf-b202-2c4f3f7334b5/json/5374/SPSE-PesertaTender/tipe/4:4/parameter/2025:93`
- Root: list berisi 4224 item

- **Struktur Bidang:**
    ```json
{
        "kd_satker": "str",
        "nama_penyedia": "str",
        "npwp_penyedia": "str",
        "kd_satker_str": "str",
        "kd_peserta": "int",
        "kd_tender": "int",
        "kd_pkt_dce": "int",
        "npwp_penyedia_16": "str",
        "kd_klpd": "str",
        "nilai_penawaran": "null",
        "pemenang_terverifikasi": "int",
        "alasan": "null",
        "nilai_terkoreksi": "null",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "kd_penyedia": "int",
        "pemenang": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `nama_penyedia` memiliki beberapa tipe: `null, str`
  - Field `npwp_penyedia` memiliki beberapa tipe: `null, str`
  - Field `kd_peserta` memiliki beberapa tipe: `int, null`
  - Field `npwp_penyedia_16` memiliki beberapa tipe: `null, str`
  - Field `nilai_penawaran` memiliki beberapa tipe: `float, int, null`
  - Field `pemenang_terverifikasi` memiliki beberapa tipe: `int, null`
  - Field `nilai_terkoreksi` memiliki beberapa tipe: `float, int, null`
  - Field `kd_penyedia` memiliki beberapa tipe: `int, null`
  - Field `pemenang` memiliki beberapa tipe: `int, null`

## 43. [1076] SPSE-TenderEkontrak-4BAPBAST

- Kelompok: SPSE
- Deskripsi: Data Tender EKontrak yang sudah menginputkan BAP BAST oleh PPK pada SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/9fdb94fc-8c9a-44c8-a7a3-b28a857f3ef6/json/5978/SPSE-TenderEkontrak-BAPBAST/tipe/4:4/parameter/2025:93`
- Status: Gagal memuat data (File JSON kosong)

## 44. [1073] SPSE-TenderEkontrak-2Kontrak

- Kelompok: SPSE
- Deskripsi: Data Tender EKontrak yang sudah menginputkan Kontrak oleh PPK pada SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/5e256e07-ff5e-4293-9899-d1ca88377aeb/json/5526/SPSE-TenderEkontrak-Kontrak/tipe/4:4/parameter/2025:93`
- Root: list berisi 52 item

- **Struktur Bidang:**
    ```json
{
        "alasan_nilai_kontrak_10_persen": "null",
        "tgl_penetapan_status_kontrak": "null",
        "nama_paket": "str",
        "kd_tender": "int",
        "bentuk_usaha_penyedia": "str",
        "kd_satker": "str",
        "wakil_sah_penyedia": "str",
        "nilai_umk_kontrak": "int",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "versi_addendum": "int",
        "apakah_addendum": "str",
        "jabatan_wakil_penyedia": "str",
        "kota_kontrak": "str",
        "tgl_kontrak_akhir": "str",
        "alamat_satker": "str",
        "status_kontrak": "str",
        "alasan_addendum": "null",
        "kd_penyedia": "int",
        "nama_penyedia": "str",
        "npwp_penyedia": "str",
        "kd_satker_str": "str",
        "nama_klpd": "str",
        "nama_pemilik_rek_bank": "str",
        "anggota_kso": "null",
        "jenis_kontrak": "str",
        "no_rek_bank": "str",
        "nilai_kontrak": "int",
        "tgl_kontrak_awal": "str",
        "nilai_pdn_kontrak": "int",
        "alasan_penetapan_status_kontrak": "null",
        "nama_rek_bank": "str",
        "jenis_klpd": "str",
        "lingkup_pekerjaan": "str",
        "no_kontrak": "str",
        "npwp_16_penyedia": "str",
        "alasan_ubah_nilai_kontrak": "str",
        "informasi_lainnya": "str",
        "jabatan_ppk": "str",
        "nama_satker": "str",
        "nama_ppk": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "no_sk_ppk": "str",
        "no_sppbj": "str",
        "tgl_kontrak": "str",
        "tipe_penyedia": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `nilai_umk_kontrak` memiliki beberapa tipe: `float, int`
  - Field `nilai_kontrak` memiliki beberapa tipe: `float, int`
  - Field `nilai_pdn_kontrak` memiliki beberapa tipe: `float, int`

## 45. [1077] SPSE-TenderEkontrak-3SPMKSPP

- Kelompok: SPSE
- Deskripsi: Data Tender EKontrak yang sudah menginputkan SPMK/SPP oleh PPK pada SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/abcd3c5e-3512-4848-80fa-4739c00cdbd1/json/6078/SPSE-TenderEkontrak-SPMKSPP/tipe/4:4/parameter/2025:93`
- Root: list berisi 45 item

- **Struktur Bidang:**
    ```json
{
        "nama_paket": "str",
        "tgl_selesai_pekerjaan": "str",
        "kota_spmk_spp": "str",
        "kd_tender": "int",
        "kd_satker": "str",
        "wakil_sah_penyedia": "str",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "jabatan_wakil_penyedia": "str",
        "no_spmk_spp": "str",
        "waktu_penyelesaian": "str",
        "alamat_satker": "str",
        "tgl_mulai_pekerjaan": "str",
        "nama_penyedia": "str",
        "alamat_penyedia": "str",
        "kd_satker_str": "str",
        "npwp_penyedia": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "alamat_pengiriman": "null",
        "tgl_spmk_spp": "str",
        "jenis_klpd": "str",
        "no_kontrak": "str",
        "npwp_penyedia_16": "str",
        "jabatan_ppk": "str",
        "nama_satker": "str",
        "nama_ppk": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "no_sppbj": "str"
    }
    ```

## 46. [1075] SPSE-TenderEkontrak-1SPPBJ

- Kelompok: SPSE
- Deskripsi: Data Tender EKontrak yang sudah menginputkan SPPBJ oleh PPK pada SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/4ec87458-8ad9-4016-9060-517b8b1a9fed/json/5878/SPSE-TenderEkontrak-SPPBJ/tipe/4:4/parameter/2025:93`
- Root: list berisi 47 item

- **Struktur Bidang:**
    ```json
{
        "lampiran_sppbj": "str",
        "tgl_penetapan_status_kontrak": "null",
        "nama_paket": "str",
        "kd_tender": "int",
        "harga_final": "int",
        "kd_satker": "str",
        "nilai_jaminan_pelaksanaan": "int",
        "kd_klpd": "str",
        "nip_ppk": "str",
        "versi_addendum": "int",
        "tgl_sppbj": "str",
        "alamat_satker": "str",
        "kota_sppbj": "str",
        "status_kontrak": "str",
        "alasan_addendum": "null",
        "masa_berlaku_jaminan": "int",
        "nama_penyedia": "str",
        "npwp_penyedia": "str",
        "kd_satker_str": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "alasan_penetapan_status_kontrak": "null",
        "jenis_klpd": "str",
        "npwp_penyedia_16": "str",
        "jabatan_ppk": "str",
        "nama_satker": "str",
        "nama_ppk": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int",
        "no_sppbj": "str",
        "apakah_addendum": "str"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `harga_final` memiliki beberapa tipe: `float, int`

## 47. [1013] SPSE-TenderPengumuman

- Kelompok: SPSE
- Deskripsi: Layanan Tender Pengumuman dari Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/b59da058-7ae6-420d-96bf-39c9f2c8fe02/json/5350/SPSE-TenderPengumuman/tipe/4:4/parameter/2025:93`
- Root: list berisi 92 item

- **Struktur Bidang:**
    ```json
{
        "sumber_dana": "str",
        "ket_diulang": "null",
        "nama_paket": "str",
        "kd_tender": "int",
        "versi_tender": "int",
        "kd_satker": "str",
        "nama_lpse": "str",
        "lokasi_pekerjaan": "str",
        "mtd_pemilihan": "str",
        "kd_klpd": "str",
        "hps": "float",
        "kontrak_pembayaran": "str",
        "nip_ppk": "str",
        "kd_rup": "str",
        "tgl_kolektif_kolegial": "str",
        "url_lpse": "str",
        "jenis_pengadaan": "str",
        "mtd_evaluasi": "str",
        "kd_satker_str": "str",
        "nip_pokja": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "ket_ditutup": "null",
        "tgl_buat_paket": "str",
        "nama_pokja": "str",
        "status_tender": "str",
        "kualifikasi_paket": "null",
        "mtd_kualifikasi": "str",
        "pagu": "int",
        "tanggal_status": "str",
        "jenis_klpd": "str",
        "kd_pkt_dce": "int",
        "tgl_pengumuman_tender": "str",
        "list_tahun_anggaran": "str",
        "nama_satker": "str",
        "nama_ppk": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `hps` memiliki beberapa tipe: `float, int`
  - Field `ket_ditutup` memiliki beberapa tipe: `null, str`
  - Field `kualifikasi_paket` memiliki beberapa tipe: `null, str`

## 48. [1014] SPSE-TenderSelesai

- Kelompok: SPSE
- Deskripsi: Layanan Tender Selesai dari Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/3edbadd7-85cd-45b7-a1a8-3ad1c0898438/json/5347/SPSE-TenderSelesai/tipe/4:4/parameter/2025:93`
- Root: list berisi 68 item

- **Struktur Bidang:**
    ```json
{
        "sumber_dana": "str",
        "nama_paket": "str",
        "tgl_penetapan_pemenang": "str",
        "kd_tender": "int",
        "kd_satker": "str",
        "nama_lpse": "str",
        "mtd_pemilihan": "str",
        "kd_klpd": "str",
        "hps": "int",
        "kontrak_pembayaran": "str",
        "url_lpse": "str",
        "kd_rup": "str",
        "mak": "str",
        "jenis_pengadaan": "str",
        "mtd_evaluasi": "str",
        "kd_satker_str": "str",
        "nama_klpd": "str",
        "status_tender": "str",
        "kualifikasi_paket": "str",
        "mtd_kualifikasi": "str",
        "pagu": "int",
        "jenis_klpd": "str",
        "kd_pkt_dce": "int",
        "tgl_pengumuman_tender": "str",
        "nama_satker": "str",
        "tahun_anggaran": "int",
        "kd_lpse": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `hps` memiliki beberapa tipe: `float, int`
  - Field `kualifikasi_paket` memiliki beberapa tipe: `null, str`

## 49. [1015] SPSE-TenderSelesaiNilai

- Kelompok: SPSE
- Deskripsi: Layanan Tender Selesai dengan Nilai Harga dan Pememang Penyedia dari Aplikasi SPSE
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/e82e66f2-b7d3-423a-89dc-c93005b5fec2/json/5348/SPSE-TenderSelesaiNilai/tipe/4:4/parameter/2025:93`
- Root: list berisi 77 item

- **Struktur Bidang:**
    ```json
{
        "tgl_penetapan_pemenang": "str",
        "kd_rup_paket": "str",
        "kd_tender": "int",
        "kd_satker": "str",
        "nilai_negosiasi": "float",
        "nilai_umk_kontrak": "float",
        "kd_klpd": "str",
        "hps": "float",
        "kd_lpse": "int",
        "nama_penyedia": "str",
        "npwp_penyedia": "str",
        "_event_date": "str",
        "nama_klpd": "str",
        "kd_paket": "int",
        "nilai_terkoreksi": "float",
        "pagu": "int",
        "nilai_pdn_kontrak": "float",
        "jenis_klpd": "str",
        "npwp_16_penyedia": "str",
        "nilai_penawaran": "float",
        "tgl_pengumuman_tender": "str",
        "nama_satker": "str",
        "tahun_anggaran": "int",
        "nilai_kontrak": "float",
        "kd_penyedia": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `nilai_negosiasi` memiliki beberapa tipe: `float, int, null`
  - Field `nilai_umk_kontrak` memiliki beberapa tipe: `float, int, null`
  - Field `hps` memiliki beberapa tipe: `float, int`
  - Field `nama_penyedia` memiliki beberapa tipe: `null, str`
  - Field `npwp_penyedia` memiliki beberapa tipe: `null, str`
  - Field `nilai_terkoreksi` memiliki beberapa tipe: `float, int, null`
  - Field `nilai_pdn_kontrak` memiliki beberapa tipe: `float, int, null`
  - Field `npwp_16_penyedia` memiliki beberapa tipe: `null, str`
  - Field `nilai_penawaran` memiliki beberapa tipe: `float, int, null`
  - Field `nilai_kontrak` memiliki beberapa tipe: `float, int, null`
  - Field `kd_penyedia` memiliki beberapa tipe: `int, null`

## 50. [1213] Ecat-PaketEPurchasingV6

- Kelompok: PURCHASING
- Deskripsi: data transaksi pada eKatalog v6 dengan status_pengiriman 'completed'
- Endpoint: `https://isb.lkpp.go.id/isb-2/api/fb0a9780-8b9e-43d4-9b48-630595a52eee/json/30993/Ecat-PaketEPurchasingV6/tipe/4:12/parameter/2025:D107`
- Root: list berisi 606 item

- **Struktur Bidang:**
    ```json
{
        "sumber_dana": "str",
        "kd_penyedia_sikap": "int",
        "kd_penyedia_v6": "str",
        "kd_klpd": "str",
        "jenis_instansi": "str",
        "kd_rup": "str",
        "mak": "str",
        "status_pengiriman": "str",
        "jml_produk": "int",
        "jml_jenis_produk": "int",
        "kd_satker_str": "str",
        "ongkir": "int",
        "product_ids": "str",
        "kd_paket": "str",
        "total_harga": "int",
        "nama_instansi": "str",
        "tgl_order": "str",
        "status_pkt": "str",
        "rup_nama_pkt": "str",
        "nama_satker": "str",
        "tahun_anggaran": "int"
    }
    ```

- **Catatan Variasi Tipe Data:**
  - Field `jml_produk` memiliki beberapa tipe: `float, int`

