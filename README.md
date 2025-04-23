# Project-imageclassification-DBS
Repositori ini berisi hasil pelatihan model image classification yang telah dikonversi ke dalam tiga format berbeda: TensorFlow SavedModel, TensorFlow.js, dan TensorFlow Lite. Tujuan dari konversi ini adalah agar model dapat digunakan di berbagai platform seperti backend server, aplikasi web, dan perangkat mobile.

## Struktur Direktori

```
submission
├───saved_model        # Format asli TensorFlow SavedModel (deployment umum)
│   ├───saved_model.pb
│   ├───variables
│   ├───assets         # (opsional) resource tambahan
│   └───fingerprint.pb # metadata integritas model
│
├───tfjs_model         # Format model untuk TensorFlow.js (web deployment)
│   ├───model.json
│   └───group1-shard*.bin
│
├───tflite             # Format model untuk TensorFlow Lite (mobile/embedded)
│   ├───model.tflite
│   └───label.txt
│
├───notebook.ipynb     # Notebook proses pelatihan dan konversi model
├───requirements.txt   # Daftar library Python yang digunakan
└───README.md          # Deskripsi proyek ini
```

## Penjelasan Format Model

- **SavedModel**: Format default TensorFlow yang bisa digunakan untuk serving atau deploy ke cloud.
- **TensorFlow.js (TFJS)**: Model yang telah dikonversi agar bisa digunakan langsung di browser.
- **TensorFlow Lite (TFLite)**: Model ringan untuk perangkat mobile/embedded seperti Android atau Raspberry Pi.

## Cara Penggunaan

- Untuk menjalankan ulang proses pelatihan atau konversi, buka dan jalankan file `notebook.ipynb`.
- Pastikan library yang dibutuhkan terpasang dengan menjalankan:

  ```bash
  pip install -r requirements.txt
  ```

---

**Catatan:** Semua file tambahan seperti `assets`, `fingerprint.pb`, dan banyaknya `.bin` di folder TFJS adalah bagian dari struktur normal model dan **tidak perlu dihapus**.

```
