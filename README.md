# Notes Ontology Project SOSRS (Symptom Oriented Specialist Recommender System)

## Class
```
Thing
├── Kondisi
├── Gejala
│   ├── Ngilu
│   ├── NyeriMalamHari
│   ├── NyeriSaatMenggigit
│   └── NyeriSpontan
├── Pasien
├── Pemicu
│   ├── TekananSaatMenggigit
│   ├── StimulusDingin
│   └── StimulusPanas
├── PenyakitGigi
│   ├── Gingivitis
│   ├── HipersensitivitasDentin
│   ├── Periodontitis
│   ├── PulpitisIrreversible
│   └── PulpitisReversible
└── SpesialisGigi
    ├── DokterGigiUmum
    ├── SpesialisEndodentis
    └── SpesialisPeridonsia
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