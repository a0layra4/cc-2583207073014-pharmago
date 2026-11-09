# ADR-0001: Initial VPS Deployment Architecture

## Status
Accepted

## Context
VPS Ubuntu Server 24.04 (Azure) dengan RAM sekitar 1 GB. Proyek PharmaGo membutuhkan deployment yang ringan, aman, dan mudah dikembangkan.

## Decision
- Flask sebagai aplikasi web
- Gunicorn dengan 1 worker dan 2 thread
- systemd sebagai service manager
- Caddy sebagai reverse proxy
- UFW sebagai firewall host
- GitHub sebagai repository

## Alternatives
1. Node.js + PM2
2. NGINX + Gunicorn
3. Docker
4. PHP-FPM

## Rationale
Python 3.12 adalah default Ubuntu 24.04. Gunicorn dan Caddy ringan untuk RAM terbatas. Caddy menyiapkan HTTPS otomatis untuk M04. Container belum dipakai karena menjadi materi M06.

## Consequences
### Positive
- Footprint kecil (service sekitar 30 MB)
- Backend tidak terekspos publik
- Mudah direproduksi dari repository

### Negative
- Single VPS tanpa redundansi
- Deployment masih manual
- HTTP saja sampai M04

## Review Trigger
Review pada M06/M07.
