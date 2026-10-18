# Requirements

## Problem Statement
Petugas perpustakaan membutuhkan cara untuk mencatat dan memantau peminjaman buku secara terpusat. Sistem menyediakan pencatatan buku, anggota, peminjaman, dan status pengembalian sehingga buku yang sedang dipinjam dan keterlambatan dapat ditelusuri.

## Target Users
- Petugas perpustakaan
- Anggota perpustakaan

## User Needs
- Sebagai petugas perpustakaan, saya ingin melihat buku yang belum dikembalikan, sehingga saya dapat menindaklanjuti keterlambatan.
- Sebagai anggota perpustakaan, saya ingin mengetahui ketersediaan sebuah buku, sehingga saya tidak datang sia-sia.

## Functional Requirements
- FR-01 Sistem menampilkan halaman utama.
- FR-02 Sistem menyediakan health endpoint.
- FR-03 Sistem menampilkan metadata aplikasi.
- FR-04 Sistem menampilkan daftar objek utama proyek.

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
