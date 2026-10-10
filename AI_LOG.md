```markdown
# AI Usage Log

## Milestones: sec-0.1
- **Tanggal:** 9 Oktober 2026
- **Prompt yang digunakan:** Menyusun Inventaris Aset, DFD, Threat Modeling STRIDE, Evaluasi Risiko, dan Rencana Kontrol Keamanan untuk aplikasi Toko Online.
- **Hasil yang digenerate:** Dokumen `security/threat-model.md` yang mencakup klasifikasi CIA, diagram DFD Mermaid dengan trust boundary, 10 ancaman STRIDE, 5 risiko prioritas, dan mitigasi kontrol.

### Manipulasi Harga Checkout (Tampering)

Kemungkinan: Tinggi | Dampak: Tinggi | Tingkat Risiko: KRITIS

Justifikasi: Sangat mudah diubah dari sisi browser/client jika tidak di-check ulang oleh server, berdampak kerugian finansial langsung.

### SQL Injection Database (Tampering)

Kemungkinan: Sedang | Dampak: Sangat Tinggi | Tingkat Risiko: KRITIS

Justifikasi: Berisiko menghapus seluruh database toko atau mencuri data sensitif pelanggan.

### Celah IDOR Hak Akses (Elevation of Privilege)

Kemungkinan: Tinggi | Dampak: Tinggi | Tingkat Risiko: TINGGI

Justifikasi: Pengguna biasa bisa mengubah parameter ID pada URL untuk mengambil alih hak akses akun admin.

### Kebocoran Storage Backup (Information Disclosure)

Kemungkinan: Sedang | Dampak: Tinggi | Tingkat Risiko: TINGGI

Justifikasi: Kelalaian konfigurasi cloud storage membuat seluruh data PII dan riwayat pembayaran bocor ke publik.

### DoS pada Endpoint Checkout (Denial of Service)

Kemungkinan: Tinggi | Dampak: Sedang | Tingkat Risiko: TINGGI

Justifikasi: Tumbangnya server saat event promo mengakibatkan pembeli tidak bisa bertransaksi.