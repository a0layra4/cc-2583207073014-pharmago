# Requirements

## Problem Statement
Masyarakat sering kesulitan mengetahui ketersediaan obat di apotek terdekat, harus mengantre untuk menebus resep dokter, serta bingung memilih obat yang sesuai dengan keluhan ringan. Sistem menyediakan layanan pemesanan dan pengantaran obat online dari apotek terdekat, fitur unggah/input resep dokter, serta rekomendasi obat berdasarkan keluhan pengguna.

## Target Users
- Pembeli / Pasien
- Admin Apotek

## User Needs
- Sebagai pembeli, saya ingin memesan obat dari apotek terdekat atau memilih apotek tertentu, sehingga obat dapat diantar langsung ke rumah tanpa harus mengantre.
- Sebagai pembeli, saya ingin memasukkan resep dokter dan mendapatkan rekomendasi obat sesuai keluhan, sehingga saya dapat membeli obat yang tepat dengan mudah.
- Sebagai admin apotek, saya ingin memantau pesanan masuk dan daftar resep yang dikirim pembeli, sehingga proses penyiapan dan pengiriman obat lebih terorganisir.

## Functional Requirements
- FR-01 Sistem menampilkan halaman utama.
- FR-02 Sistem menyediakan health endpoint.
- FR-03 Sistem menampilkan metadata aplikasi.
- FR-04 Sistem menampilkan daftar objek utama proyek (apotek, obat, resep, pesanan).

## Non-Functional Requirements
- NFR-01 Backend hanya listen pada loopback.
- NFR-02 Aplikasi dikelola systemd.
- NFR-03 Request publik masuk melalui reverse proxy.
- NFR-04 Secret tidak disimpan pada Git repository.
- NFR-05 Health endpoint mengembalikan HTTP 200 saat sehat.
- NFR-06 Deployment dapat direproduksi dari repository.
- NFR-07 Arsitektur sesuai VPS kecil (RAM sekitar 1 GB).

## Scope M03
In scope: repository, requirements, architecture, ADR, baseline Flask app, SSH hardening dasar, Gunicorn, systemd, Caddy, HTTP public deployment.
Out of scope: database production, Docker, IaC, CI/CD, TLS/domain, horizontal scaling, monitoring penuh.

## Constraints
- RAM sekitar 1 GB (892 MiB tersedia)
- Ubuntu Server 24.04
- public IPv4

## Acceptance Criteria M03
- [ ] first deployment accessible
- [ ] health endpoint works
