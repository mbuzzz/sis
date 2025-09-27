# 📑 Use Case Tabel — Sistem Informasi Sekolah (SIS)

## 1. Presensi RFID
| **Use Case**        | Presensi RFID Siswa                                                                 |
|----------------------|--------------------------------------------------------------------------------------|
| **Aktor**           | Siswa, Guru, Sistem RFID                                                            |
| **Tujuan**          | Mencatat kehadiran siswa secara otomatis dan cepat                                   |
| **Alur Utama**      | 1) Siswa tap kartu RFID di device <br> 2) Device kirim event ke server <br> 3) Server validasi (hash UID + jadwal aktif) <br> 4) Presensi tercatat di kelas & dashboard guru |
| **Hasil**           | Kehadiran siswa tersimpan realtime, duplikasi tap ditolak                            |

---

## 2. Kurikulum Merdeka (KM)
| **Use Case**        | Guru Membuat Modul Ajar & Rapor KM                                                   |
|----------------------|--------------------------------------------------------------------------------------|
| **Aktor**           | Guru, Waka Kurikulum                                                                |
| **Tujuan**          | Menyusun Modul Ajar sesuai CP/TP/ATP & menghasilkan rapor naratif Kurikulum Merdeka |
| **Alur Utama**      | 1) Guru pilih fase → CP → TP → ATP <br> 2) Susun Modul Ajar (rubrik, asesmen) <br> 3) Input nilai formatif/sumatif <br> 4) Sistem generate rapor PDF + narasi P5 |
| **Hasil**           | Modul ajar lengkap, nilai & rapor KM terbit otomatis dengan tanda tangan elektronik |

---

## 3. LMS — Tugas
| **Use Case**        | Pengumpulan & Penilaian Tugas                                                        |
|----------------------|--------------------------------------------------------------------------------------|
| **Aktor**           | Siswa, Guru                                                                         |
| **Tujuan**          | Siswa mengumpulkan tugas, guru memberi nilai dengan rubrik                          |
| **Alur Utama**      | 1) Siswa upload file tugas <br> 2) Guru buka submissions <br> 3) Guru menilai via rubrik & feedback <br> 4) Nilai tersimpan ke gradebook |
| **Hasil**           | Nilai tugas tercatat, siswa menerima umpan balik guru                                |

---

## 4. LMS — Kuis / CBT
| **Use Case**        | Siswa Mengerjakan Kuis                                                              |
|----------------------|--------------------------------------------------------------------------------------|
| **Aktor**           | Siswa, Guru                                                                         |
| **Tujuan**          | Mengadakan ujian singkat/kuis online berbasis bank soal                             |
| **Alur Utama**      | 1) Guru membuat kuis dari bank soal <br> 2) Siswa login & mulai kuis (timer aktif) <br> 3) Sistem auto-grade soal objektif <br> 4) Guru menilai soal essay <br> 5) Nilai otomatis masuk gradebook |
| **Hasil**           | Nilai kuis tersedia, analitik kesulitan soal dapat dilihat guru                      |

---

## 5. Live Class (Zoom)
| **Use Case**        | Kelas Daring via Zoom                                                                |
|----------------------|--------------------------------------------------------------------------------------|
| **Aktor**           | Guru, Siswa, Zoom API                                                               |
| **Tujuan**          | Mengadakan kelas online terintegrasi dengan absensi otomatis & rekaman               |
| **Alur Utama**      | 1) Guru buat jadwal Live Class (Zoom API) <br> 2) Siswa join via portal <br> 3) Zoom webhook kirim data peserta <br> 4) Sistem sinkron presensi otomatis <br> 5) Rekaman tersedia di course |
| **Hasil**           | Kelas daring berjalan, absensi otomatis, rekaman dapat diputar ulang                 |

---

## 6. PPDB
| **Use Case**        | Pendaftaran Peserta Didik Baru (PPDB)                                                |
|----------------------|--------------------------------------------------------------------------------------|
| **Aktor**           | Calon Siswa, TU                                                                     |
| **Tujuan**          | Mengelola penerimaan siswa baru secara online                                       |
| **Alur Utama**      | 1) Calon siswa isi form online + upload dokumen <br> 2) TU verifikasi <br> 3) Sistem generate nomor induk otomatis |
| **Hasil**           | Data siswa baru tersimpan di database, siap masuk ke kelas                           |

---

## 7. Keuangan
| **Use Case**        | Pembayaran Tagihan & Kwitansi                                                        |
|----------------------|--------------------------------------------------------------------------------------|
| **Aktor**           | Orang Tua, Bagian Keuangan                                                           |
| **Tujuan**          | Mengelola pembayaran manual (transfer/uang tunai)                                   |
| **Alur Utama**      | 1) Keuangan membuat tagihan <br> 2) Orang tua bayar & upload bukti <br> 3) Keuangan verifikasi <br> 4) Sistem ubah status invoice → paid <br> 5) Kwitansi PDF terbit |
| **Hasil**           | Transaksi pembayaran tercatat resmi, kwitansi dapat diunduh                          |

---

## 8. Perpustakaan
| **Use Case**        | Peminjaman & Pengembalian Buku                                                       |
|----------------------|--------------------------------------------------------------------------------------|
| **Aktor**           | Siswa, Pustakawan                                                                    |
| **Tujuan**          | Mengelola sirkulasi buku di perpustakaan                                             |
| **Alur Utama**      | 1) Pustakawan scan barcode buku + kartu siswa <br> 2) Sistem catat peminjaman <br> 3) Saat kembali, sistem hitung denda jika lewat |
| **Hasil**           | Buku terkelola rapi, status pinjaman/denda jelas                                     |

---

## 9. Orang Tua Monitoring
| **Use Case**        | Monitoring Anak                                                                      |
|----------------------|--------------------------------------------------------------------------------------|
| **Aktor**           | Orang Tua                                                                            |
| **Tujuan**          | Memantau kehadiran, nilai, rapor, dan tagihan anak                                   |
| **Alur Utama**      | 1) Ortu login portal <br> 2) Lihat ringkasan presensi & nilai <br> 3) Unduh rapor <br> 4) Cek tagihan & kwitansi |
| **Hasil**           | Orang tua mendapat informasi lengkap & transparan tentang anak                      |
