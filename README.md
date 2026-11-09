# PharmaGo

Cloud Computing — PTI 2802
Pertemuan 3 — Project Inception

## Author
Seyra Salma A Mutia Rani / 2583207073014

## Problem
Masyarakat sering kesulitan mengetahui ketersediaan obat di apotek terdekat, harus mengantre untuk menebus resep dokter, serta bingung memilih obat yang sesuai dengan keluhan ringan. Sistem menyediakan layanan pemesanan dan pengantaran obat online dari apotek terdekat, fitur unggah resep dokter, serta rekomendasi obat berdasarkan keluhan pengguna.

## Target Users
- Pembeli / Pasien
- Admin Apotek

## Features M03
- baseline application
- health endpoint
- VPS deployment

## Architecture
Internet -> UFW -> Caddy :80 -> Gunicorn 127.0.0.1:8000 -> Flask

## Infrastructure
- Ubuntu Server 24.04
- Caddy, Gunicorn, systemd, UFW
- Azure VM (spesifikasi aktual dicatat di docs/evidence/m03/notes.md)

## Public Endpoint
http://20.41.99.231/

## Health Check
GET /health

## Deployment
Lihat docs/deployment.md.

## Security
- key-only SSH
- root SSH disabled
- UFW enabled
- backend loopback-only

## Current Limitations
- HTTP only
- no persistent database
- no container
- manual deployment

## Roadmap
M04 DNS/HTTPS, M05 Data, M06 Container, M07 IaC, M09 CI/CD
