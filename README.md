# Notes Ontology Project: SOSRS (Symptom Oriented Specialist Recommender System) Spesialis Gigi

## Progress Report
### Progress Per 18 November 2025
1. Update ontology Classes, Object Properties, dan Individuals untuk mengakomodasi inferensi penyakit Pulpitis Irreversible
2. Update Plan (Revisi Classes dan Object Properties yang baru atau yang sebelumnya diubah)

### Progress Per 25 November 2025
1. Konsultasi dengan Dokter Gigi Umum untuk proses diagnosa penyakit gigi berdasarkan kondisi gigi dan gejalanya, serta spesialis yang mungkin akan dibutuhkan untuk menangani penyakit tersebut.
2. Update ontology Classes, Object Properties, dan Individuals untuk mengakomodasi inferensi penyakit Periodontitis dan Trauma Oklusi (Spesialis Endodonti dan Peridonsia)
3. Update SWRL Rule untuk inferensi penyakit Periodontitis dan Trauma Oklusi
4. Update DL Expressivity (Initial testing) untuk meningkatkan dari ALU menjadi SROIQ (Sesuai Quiz-quiz sebelumnya)
5. Update README.md pada GitHub untuk mengakomodasi Classes, Object Properties, dan Individuals baru.
6. Update laporan dalam bentuk P5

### Progress Per 2 Desember 2025
1. Konsultasi lebih dalam mengenai proses diagnosa penyakit dan penentuan spesialis berdasarkan gejala.
2. Update Ontology: Classes, Object Properties, Individuals, dan axioms untuk gejala-gejala yang dapat berkembang dan menyebabkan gejala yang lebih dalam.
3. Update SWRL rule untuk inferensi penyakit Impaksi Molar
4. Memfokuskan proyek pada inferensi 3 spesialis saja, yaitu Bedah Mulut, Endodentis, dan Peridonsia.
5. Test penambahan Annotations menggunakan KB Bioontology untuk beberapa Penyakit yang sebelumnya telah dibentuk classnya.
6. Riset dan inisiasi proyek aplikasi web untuk praktik ontology. (Untuk saat ini akan menggunakan NextJS Typescript).

### Progress Per 9 Desember 2025
1. Penambahan SWRL rule untuk penyakit-penyakit baru.
2. Update Ontology classes, axioms, properties, dll.
3. Update DL Expressivity SROIQ -> SROIQ(D): Penambahan Data Properties "Lingering Pain" dalam detik.
4. **(On going)** Update README.md pada GitHub untuk mengakomodasi Classes, Object Properties, dan Individuals baru.

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
│   ├── KarangGigi
│   └── PlakGigi
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
├── berkaitanDengan
├── berkembangMenjadi
├── dialamiOleh
├── didugaMenderita
├── dipicuOleh
├── membutuhkanSpesialis
├── memilikiGejala
├── mengalamiGejala
├── mengalamiKondisi
├── menyebabkan
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