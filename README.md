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
│   ├── BengkakWajah
│   ├── FistulaGusi
│   ├── GusiBenjol
│   ├── GusiBerdarah
│   ├── Ngilu
│   ├── Nyeri
│   │   ├── NyeriHebat
│   │   ├── NyeriMalamHari
│   │   ├── NyeriMenelan
│   │   ├── NyeriPalpasi
│   │   ├── NyeriPerkusi
│   │   ├── NyeriRahangBelakang
│   │   ├── NyeriSaatMenggigit
│   │   └── NyeriSpontan
│   ├── ResponGigiNegatif
│   ├── ResponGigiPositifKuat
│   └── Trismus
├── KondisiMulut
│   ├── KondisiGigi
│   │   ├── BauMulut
│   │   ├── DentinTerbuka
│   │   ├── GigiBerlubang
│   │   │   ├── GigiBerlubangBesar
│   │   │   ├── GigiBerlubangDalam
│   │   │   ├── GigiBerlubangKecil
│   │   │   └── GigiBerlubangSedang
│   │   ├── GigiBerwarna
│   │   │   ├── GigiGelap (Equivalent: Discoloration)
│   │   │   └── GigiKekuningan
│   │   ├── GigiErupsi
│   │   │   ├── GigiErupsiSebagian
│   │   │   └── GigiErupsiSempurna
│   │   ├── LubangPascaCabut
│   │   ├── PlakGigi
│   │   ├── PosisiGigi
│   │   │   ├── PosisiHorizontal
│   │   │   └── PosisiMiring
│   │   ├── RiwayatCabutGigi
│   │   ├── SisaAkar
│   │   └── TandaKerusakanJaringan
│   │       ├── GigiGoyang
│   │       ├── GusiTurun
│   │       └── KantungGusiDalam
│   └── KondisiGusi
├── Pemicu
│   ├── StimulusAsam
│   ├── StimulusDingin
│   ├── StimulusPanas
│   └── TekananSaatMenggigit
├── PenyakitGigi
│   ├── KelainanStruktural
│   │   ├── ImpaksiMolar
│   │   ├── InfeksiPascaCabut
│   │   ├── PeriapikalKronis
│   │   └── RadiksRelikta
│   ├── PenyakitPeriodontal
│   │   ├── AbsesPeriodontal
│   │   ├── Gingivitis
│   │   └── Periodontitis
│   ├── PenyakitPulpa
│   │   ├── AbsesPeriapikal
│   │   │   └── AbsesPeriapikalAkut
│   │   ├── HipersensitivitasDentin
│   │   ├── NekrosisPulpa
│   │   ├── PulpitisIrreversible
│   │   └── PulpitisReversible
│   └── TraumaOklusi
├── SpesialisGigi
│   ├── DokterGigiUmum
│   ├── SpesialisBedahMulut
│   ├── SpesialisEndodentis
│   └── SpesialisPeriodonsia
└── Pasien
```

## Object Properties
```
topObjectProperty
├── berkaitanDengan (Symmetric)
├── berkembangMenjadi (Asymmetric, Irreflexive)
├── dialamiOleh (Inverse of mengalamiGejala)
├── didugaMenderita (Pasien -> PenyakitGigi)
├── dipicuOleh (Gejala/Kondisi -> Pemicu)
├── dirujukKe (Pasien -> SpesialisGigi)
├── membutuhkanSpesialis (PenyakitGigi -> SpesialisGigi)
├── memilikiGejala (PenyakitGigi -> Gejala)
├── menanganiPenyakit (Inverse of membutuhkanSpesialis)
├── mengalamiGejala (Pasien -> Gejala)
├── mengalamiKondisi (Pasien -> KondisiGigi)
├── menyebabkan (Transitive)
└── tingkatUrgensi
```

## Individuals
```
Individuals
├── Pasien
│   ├── Pasien_1
│   ├── Pasien_2 (Pulpitis Irreversible)
│   ├── Pasien_Impaksi_Molar
│   ├── Pasien_Infeksi_Pasca_Cabut
│   ├── Pasien_Periapikal_Kronis
│   ├── Pasien_Periodontitis
│   └── Pasien_Trauma_Oklusi
├── Gejala
│   ├── Gejala_GusiBerdarah
│   ├── Gejala_Ngilu
│   ├── Gejala_NyeriMalamHari
│   ├── Gejala_NyeriSaatGigit
│   ├── Gejala_Nyeri_Hebat
│   ├── Gejala_Respon_Gigi_Negatif
│   ├── Gejala_Trismus
│   └── Gejala_Nyeri_Lebih_30
├── Kondisi
│   ├── Kondisi_BauMulut
│   ├── Kondisi_GigiGoyang
│   ├── Kondisi_Fistula_Gusi
│   ├── Kondisi_Gigi_Erupsi_Sebagian
│   ├── Kondisi_Lubang_Pasca_Cabut
│   ├── Kondisi_Posisi_Gigi_Miring
│   ├── Kondisi_Riwayat_Cabut_Gigi
│   └── Kondisi_Gigi_Berlubang_Besar
├── Penyakit
│   ├── Penyakit_Abses_Periapikal_Akut
│   ├── Penyakit_Abses_Periapikal_Kronis
│   ├── Penyakit_Abses_Periodontal
│   ├── Penyakit_Gingivitis
│   ├── Penyakit_Hipersensitivitas_Dentin
│   ├── Penyakit_Impaksi_Molar
│   ├── Penyakit_Infeksi_Pasca_Cabut
│   ├── Penyakit_Nekrosis_Pulpa
│   ├── Penyakit_Periodontitis
│   ├── Penyakit_Pulpitis_Irreversible
│   ├── Penyakit_Pulpitis_Reversible
│   ├── Penyakit_Radiks_Relikta
│   └── Penyakit_Trauma_Oklusi
├── Spesialis
│   ├── Spesialis_Bedah_Mulut
│   ├── Spesialis_Konservasi_Gigi
│   ├── Spesialis_Peridonsia
│   └── Spesialis_Umum
└── Pemicu
    ├── Stimulus_Dingin
    ├── Stimulus_Panas
    └── Tekanan
```