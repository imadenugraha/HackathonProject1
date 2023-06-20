# 🕹️ Project Hackathon System Administrator SEMESTA Batch 5

Nama: I Made Nugrahe Jaye Putra

Asal Sekolah: SMK N 2 Yogyakarta

## 📝 Deskripsi Project
Project ini menggunakan Ansible sebagai tools untuk melakukan build image, deploy, dan juga menghapus image. Terdapat dua file yaitu container-up.yaml yang digunakan untuk melakukan build dan deploy aplikasi. File container-down.yaml yang digunakan untuk menghapus image.

Skema penggunaan project:

Satu server yang sudah terdapat source code aplikasi yang sudah diberikan. Admin melakukan konfigruasi pada inventory seperti ip server, ansible_user, dan juga become_true. Ketika Admin mendapatkan permintaan dari developer untuk melakukan deploy, maka Admin akan menjalankan container-up.yaml terlebih dahulu jika 
belum ada image yang pernah dibuat. Namun jika sudah ada image yang pernah dibuat maka container-down.yaml akan dijalankan terlebih dahulu.

## 🚀 How To Use Script
1. Konfigurasi IP Address server pada file inventory.
```ini
[production-srv]
192.168.1.2
```

2. Ganti ansible_user pada file inventory.
```ini
[production-srv:vars]
ansible_user=ansible
```

3. Jalankan container-up.yaml menggunakan ansible-playbook command.
```bash
$ ansible-playboook container-up.yaml
```

4. Jalankan container-down.yaml menggunakan ansible-playbook command.
```bash
$ ansible-playbook container-down.yaml
```

Made with 💙 by me