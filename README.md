# Notes Ontology Project: SOSRS (Symptom Oriented Specialist Recommender System)

## Classes
```
Thing
├── Gejala
│   ├── GusiBerdarah
│   ├── Ngilu
│   ├── NyeriMalamHari
│   ├── NyeriSaatMenggigit
│   └── NyeriSpontan
├── KondisiGigi
│   ├── BauMulut
│   ├── GigiBerlubang
│   ├── GigiGoyang
│   ├── GusiTurun
│   ├── KantungGusiDalam
│   └── KarangGigi
├── Pemicu
│   ├── TekananSaatMenggigit
│   ├── StimulusDingin
│   └── StimulusPanas
├── PenyakitGigi
│   ├── Gingivitis
│   ├── HipersensitivitasDentin
│   ├── Periodontitis
│   ├── PulpitisIrreversible
│   ├── PulpitisReversible
│   └── TraumaOklusi
├── SpesialisGigi
│   ├── DokterGigiUmum
│   ├── SpesialisEndodentis
│   └── SpesialisPeridonsia
├── TandaKerusakanJaringan
│   ├── GigiGoyang (Subclass Of KondisiGigi)
│   ├── GusiTurun (Subclass Of KondisiGigi)
│   └── KantungGusiDalam (Subclass Of KondisiGigi)
└── Pasien
```

## Object Properties
```
topObjectProperty
├── memilikiGejala
├── dipicuOleh
├── membutuhkanSpesialis
├── mengalamiGejala
└── tingkatUrgensi
```

## Individuals
```
├── Gejala
│   ├── Gejala_GusiBerdarah
│   ├── Gejala_Ngilu
│   ├── Gejala_NyeriMalamHari
│   └── Gejala_NyeriSaatGigit
├── Kondisi
│   ├── Kondisi_BauMulut
│   └── Kondisi_GigiGoyang
├── Penyakit
│   ├── Penyakit_Periodontitis
│   ├── Penyakit_Pulpitis_Irreversible
│   ├── Penyakit_Pulpitis_Reversible
│   └── Penyakit_Trauma_Oklusi
├── Spesialis
│   ├── Spesialis_Konservasi_Gigi
│   └── Spesialis_Umum
└── Pemicu
    ├── Pemicu_Tekanan
    ├── Pemicu_Makanan_Panas
    └── Pemicu_Makanan_Dingin m,
```