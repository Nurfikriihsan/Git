## 🧠 Git Commands Cheat Sheet: 50+ Perintah Git

---

### 📦 Konfigurasi Awal Git

```bash
git config --global user.name "Nama Kamu"          # Mengatur nama pengguna global
git config --global user.email "email@domain.com"  # Mengatur email global
git config --global core.editor "code --wait"      # Menetapkan editor default (VSCode)
git config --list                                  # Melihat seluruh konfigurasi Git
git help <command>                                 # Bantuan untuk perintah tertentu
```

---

### 🏁 Membuat & Mengelola Repositori

```bash
git init                            # Membuat repository baru di folder saat ini
git clone <url>                     # Mengkloning repository dari remote (GitHub, GitLab, dll)
git remote add origin <url>         # Menambahkan remote repository
git remote -v                       # Melihat daftar remote yang terhubung
git remote remove origin            # Menghapus remote
```

---

### 📂 Status, Log & Informasi

```bash
git status              # Melihat status file (staged, modified, untracked)
git log                 # Melihat riwayat commit lengkap
git log --oneline       # Melihat log singkat tiap commit
git log --graph --decorate --oneline --all # Menampilkan struktur branch visual
git show <commit-id>    # Menampilkan detail commit tertentu
git diff                # Melihat perbedaan yang belum di-stage
git diff --staged       # Melihat perbedaan file yang sudah di-stage
```

---

### ✍️ Menambahkan & Commit Perubahan

```bash
git add <file>          # Menambahkan file tertentu ke staging area
git add .               # Menambahkan semua perubahan
git reset <file>        # Menghapus file dari staging area
git commit -m "Pesan"   # Commit perubahan dengan pesan
git commit -am "Pesan"  # Menambahkan dan commit sekaligus
git commit --amend      # Mengubah commit terakhir
```

---

### 🌿 Branching

```bash
git branch                      # Melihat daftar branch
git branch <nama-branch>         # Membuat branch baru
git checkout <nama-branch>       # Berpindah ke branch lain
git checkout -b <nama-branch>    # Membuat & langsung berpindah ke branch baru
git branch -d <nama-branch>      # Menghapus branch lokal
git branch -D <nama-branch>      # Menghapus branch lokal secara paksa
```

---

### 🔀 Merge & Rebase

```bash
git merge <nama-branch>          # Menggabungkan branch tertentu ke branch aktif
git merge --abort                # Membatalkan proses merge
git rebase <nama-branch>         # Menyusun ulang commit berdasarkan branch lain
git rebase --abort               # Membatalkan proses rebase
git rebase --continue            # Melanjutkan proses rebase yang tertunda
```

---

### 🚀 Push & Pull

```bash
git push origin <branch>         # Mengirim commit ke remote
git push -u origin <branch>      # Push dan set upstream branch
git push                         # Push ke upstream default
git pull                         # Mengambil perubahan dari remote dan merge
git fetch                        # Mengambil update dari remote tanpa merge
git pull --rebase                # Menarik perubahan dengan rebase
```

---

### 🧹 Undo & Reset

```bash
git restore <file>               # Mengembalikan file ke versi terakhir
git restore --staged <file>      # Menghapus file dari staging area
git reset --soft HEAD~1          # Membatalkan commit terakhir tapi simpan perubahan
git reset --hard HEAD~1          # Menghapus commit terakhir dan perubahan
git revert <commit-id>           # Membuat commit baru untuk membatalkan commit tertentu
```

---

### 🧭 Tagging

```bash
git tag                          # Melihat semua tag
git tag <nama-tag>               # Membuat tag baru
git tag -a <nama-tag> -m "Pesan" # Membuat tag dengan pesan
git push origin <nama-tag>       # Mengirim tag ke remote
git push origin --tags           # Mengirim semua tag ke remote
git tag -d <nama-tag>            # Menghapus tag lokal
```

---

### 🧩 Stash

```bash
git stash                        # Menyimpan perubahan sementara
git stash save "Pesan"            # Menyimpan perubahan dengan pesan
git stash list                   # Melihat daftar stash
git stash apply                  # Menerapkan stash terbaru tanpa menghapusnya
git stash pop                    # Terapkan dan hapus stash terbaru
git stash drop <stash@{n}>       # Menghapus stash tertentu
```

---

### 🧱 Remote Management

```bash
git remote show origin           # Menampilkan informasi detail remote
git fetch origin                 # Mengambil update dari remote tanpa merge
git pull origin main             # Mengambil update branch main
git push origin main             # Mengirim commit ke branch main
git remote rename origin upstream # Mengganti nama remote
```

---

### ⚙️ Advanced

```bash
git cherry-pick <commit-id>      # Mengambil commit tertentu ke branch aktif
git bisect start                 # Memulai pencarian commit penyebab bug
git blame <file>                 # Melihat siapa yang mengubah setiap baris file
git reflog                       # Melihat seluruh riwayat perubahan HEAD
git shortlog -sn                 # Menampilkan jumlah commit per kontributor
git gc                           # Membersihkan repository dari file tidak perlu
git fsck                         # Memeriksa integritas data repository
```

---

### 🔐 Setup SSH Key

```bash
ssh-keygen -t ed25519 -C "email@domain.com"   # Membuat SSH key baru
cat ~/.ssh/id_ed25519.pub                     # Menampilkan public key untuk disalin
ssh -T git@github.com                         # Menguji koneksi ke GitHub
```

---

## 💻 Instalasi Git (Windows, macOS, Linux)

#### 🪟 Windows

1. Unduh installer di [git-scm.com](https://git-scm.com/download/win)
2. Jalankan installer → pilih opsi default
3. Buka terminal (Git Bash) dan jalankan `git --version`

#### 🍎 macOS

```bash
brew install git
```

#### 🐧 Linux
```bash
sudo apt update
sudo apt install git -y
```

---

### 🧰 Alias

```bash
git config --global alias.st "status"
git config --global alias.co "checkout"
git config --global alias.br "branch"
git config --global alias.cm "commit -m"
git config --global alias.last "log -1 HEAD"
```

---

## 📜 License

[MIT License](./LICENSE) © 2025.
Kalau merasa terbantu, kasih ⭐ di repo ini 🙌

---

Dibuat dengan ❤️ oleh DeepCodeX


