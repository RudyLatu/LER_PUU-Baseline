# Data Card — LERPUU Dataset

## Sumber
Dokumen: Putusan Mahkamah Konstitusi (MK) Republik Indonesia.
Diambil dari: <sumber/tautan resmi MK>

## Skema Anotasi
Format label: BIO (Beginning-Inside-Outside).
Lihat panduan lengkap: `docs/Annotation_Guideline_LER_PUU_MKRI.pdf`

Contoh jenis entitas (isi sesuai skema aktual Anda):
- `PERSON` — nama orang yang tidak dapat dikategorikan secara spesifik sebagai hakim, kuasa hukum, atau pejabat lain
- `JUDGE` — nama hakim konstitusi dalam kapasitas persidangan
- `LAWYER` — nama kuasa hukum / advokat yang mewakili pihak berperkara
- `REGISTRAR` — nama panitera atau panitera pengganti yang bertugas dalam persidangan
- `LAW_NAMA` — nama lengkap peraturan perundang-undangan termasuk nomor, tahun, dan judul
- `LAW_CONS_ART` — pasal, ayat, huruf, atau angka dalam konstitusi atau undang-undang
- `LEGAL_DOC` — nama dokumen hukum prosedural yang dirujuk dalam putusan
- `LEGAL_DOC_NUM` — nomor atau identifikasi dokumen hukum prosedural
- `DECISION_NUM` — nomor resmi putusan mahkamah konstitusi
- `DECISION_DATE` — tanggal pengucapan atau penetapan putusan MKRI secara resmi
- `DATE` — tanggal umum yang muncul dalam narasi putusan selain tanggal putusan resmi
- `PARTY_REF` — Sebutan atau referensi pihak berperkara 
- `ORG` — nama lembaga, institusi, atau organisasi yang dirujuk dalam putusan
- `EVENT` — peristiwa hukum atau kegiatan persidangan yang dirujuk dalam putusan
- `DICTUM_HEAD` — penanda kepala amar - frasa pembukaan bagian amar
- `DICTUM_BODY` — isi butir amar putusan dan/atau kalimat putusan resmi per butir

## Statistik
| Split | Jumlah Dokumen | Jumlah Token | Jumlah Entitas |
|-------|-----------------|--------------|-----------------|
| Train | ...             | ...          | ...             |
| Dev   | ...             | ...          | ...             |
| Test  | ...             | ...          | ...             |

## Format File
- `processed/ID_doc_labeled_dataset.jsonl` — satu dokumen per baris JSON,
  field: `text`, `entities` (span-based) atau `tokens` + `labels`.
- `processed/conll/` — format CoNLL (satu token per baris, kolom label BIO),
  dipisah per split (`train.conll`, `dev.conll`, `test.conll`).

## Versi
- v6.1 — <catatan perubahan singkat>
- v7 — <catatan perubahan singkat, jika berbeda dari versi data>

## Lisensi Data
<Nyatakan status: dokumen putusan pengadilan umumnya bersifat publik,
tapi anotasi/label adalah karya turunan — tentukan lisensi yang berlaku,
mis. CC-BY-4.0 untuk anotasi.>
