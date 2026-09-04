# LERPUU-NER

Legal Entity Recognition untuk dokumen Peraturan Perundang-undangan (PUU) —
eksperimen Named Entity Recognition (NER) pada teks hukum Indonesia, dengan
studi kasus putusan Mahkamah Konstitusi (MK).

## Struktur Repo

```
lerpuu-ner/
├── data/
│   ├── README.md          # data card: skema label, jumlah dokumen, split
│   ├── raw/                # teks putusan MK sebelum diproses
│   └── processed/
│       ├── ID_doc_labeled_dataset.jsonl
│       └── conll/           # format CoNLL untuk training
├── docs/
│   └── Annotation_Guideline_LER_PUU_MKRI.pdf
├── notebooks/
│   ├── 01_ekstraksi_putusan_mk_cleantext.ipynb
│   ├── 02_preprocessing.ipynb
│   └── 03_baseline_model_v7.ipynb
├── src/                     # fungsi bersama yang dipakai lintas notebook
├── models/                  # checkpoint (gitignored — lihat bagian Model)
└── results/
    ├── metrics/
    └── figures/
```

## Setup

```bash
git clone <repo-url>
cd lerpuu-ner
pip install -r requirements.txt
```

Jika dataset menggunakan Git LFS:

```bash
git lfs install
git lfs pull
```

## Pipeline

1. `notebooks/01_ekstraksi_putusan_mk_cleantext.ipynb` — ekstraksi dan
   pembersihan teks putusan MK dari sumber dokumen mentah.
2. `notebooks/02_preprocessing.ipynb` — konversi ke format berlabel
   (BIO tagging, split train/dev/test).
3. `notebooks/03_baseline_model_v7.ipynb` — training dan evaluasi model
   baseline NER.

## Dataset

Lihat `data/README.md` untuk detail skema label, jumlah dokumen per split,
dan panduan anotasi lengkap ada di `docs/Annotation_Guideline_LER_PUU_MKRI.pdf`.

## Model

Checkpoint model tidak disertakan langsung di repo ini karena ukurannya besar.
Unduh dari: <tautan rilis / Hugging Face Hub / Google Drive>

## Sitasi

Jika dataset atau kode ini digunakan dalam penelitian Anda, mohon sitasi
sesuai `CITATION.cff`.

## Lisensi

Lihat `LICENSE` untuk kode. Status lisensi/penggunaan dataset dijelaskan
terpisah di `data/README.md` (mengingat dokumen sumber adalah putusan
pengadilan yang bersifat publik).
