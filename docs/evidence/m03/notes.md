# Evidence M03

- Platform: Azure VM, Ubuntu Server 24.04
- Spesifikasi aktual: 2 vCPU, RAM 892 MiB, disk 61 GB (modul menulis 1 vCPU / 1 GB / 20 GB)
- Swap 1 GB ditambahkan manual
- Deviasi dari modul: file hardening SSH dinamai 00-pti2802.conf (bukan 99-), karena 50-cloud-init.conf bawaan Azure berisi PasswordAuthentication yes dan nilai pertama yang menang
- Akses SSH key-only dengan user cloudstudent; root dan password SSH dinonaktifkan
- Gunicorn: 1 worker, 2 thread, bind 127.0.0.1:8000
- Caddy reverse proxy di port 80 (HTTP saja, HTTPS di M04)
- Service tetap aktif setelah reboot
- Endpoint publik: http://20.41.99.231/ dan /health
