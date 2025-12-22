1. p1_pulpitis_reversible_rule
Pasien(?p) ^ mengalamiGejala(?p, ?g) ^ Ngilu(?g) ^ dipicuOleh(?g, ?trig) ^ StimulusDingin(?trig) ^ autogen0:durasiNyeri(?g, ?detik) ^ swrlb:lessThanOrEqual(?detik, 10) -> didugaMenderita(?p, Penyakit_Pulpitis_Reversible)

2. p3_pulpitis_irreversible_rule1
Pasien(?p) ^ mengalamiGejala(?p, ?g) ^ Ngilu(?g) ^ dipicuOleh(?g, ?trig) ^ StimulusDingin(?trig) ^ durasiNyeri(?g, ?detik) ^ swrlb:greaterThan(?detik, 30) -> didugaMenderita(?p, Penyakit_Pulpitis_Irreversible)

3. p3_pulpitis_irreversible_rule2
Pasien(?p) ^ mengalamiGejala(?p, ?g) ^ NyeriSpontan(?g) -> didugaMenderita(?p, Penyakit_Pulpitis_Irreversible)

4. p3_pulpitis_irreversible_rule3
Pasien(?p) ^ mengalamiGejala(?p, ?g) ^ NyeriMalamHari(?g) -> didugaMenderita(?p, Penyakit_Pulpitis_Irreversible)

5. p3_nekrosis_pulpa
Pasien(?p) ^ mengalamiKondisi(?p, ?k) ^ Discoloration(?k) ^ mengalamiGejala(?p, ?g) ^ ResponGigiNegatif(?g) -> didugaMenderita(?p, Penyakit_Nekrosis_Pulpa)

6. p3_periapikal_kronis_rule1
Pasien(?p) ^ mengalamiKondisi(?p, ?k) ^ FistulaGusi(?k) ^ mengalamiGejala(?p, ?g) ^ ResponGigiNegatif(?g) -> didugaMenderita(?p, Penyakit_Abses_Periapikal_Kronis)

7. p3_abses_periapikal_akut_rule1
Pasien(?p) ^ mengalamiGejala(?p, ?g1) ^ ResponGigiNegatif(?g1) ^ mengalamiGejala(?p, ?g2) ^ NyeriPerkusi(?g2) ^ mengalamiGejala(?p, ?g3) ^ BengkakWajah(?g3) -> didugaMenderita(?p, Penyakit_Abses_Periapikal_Akut)

8. p4_gingivitis
Pasien(?p) ^ mengalamiGejala(?p, ?g) ^ GusiBerdarah(?g) ^ mengalamiKondisi(?p, ?k) ^ KarangGigi(?k) -> didugaMenderita(?p, Penyakit_Gingivitis)

9. p4_periodontitis
Pasien(?p) ^ mengalamiGejala(?p, ?g) ^ GusiBerdarah(?g) ^ mengalamiKondisi(?p, ?k) ^ GigiGoyang(?k) -> didugaMenderita(?p, Penyakit_Periodontitis)

10. p4_abses_periodontal
Pasien(?p) ^ mengalamiKondisi(?p, ?k) ^ GusiBenjol(?k) ^ mengalamiGejala(?p, ?g) ^ ResponGigiPositifKuat(?g) -> didugaMenderita(?p, Penyakit_Abses_Periodontal)

11. p_trauma_okulsi
Pasien(?p) ^ mengalamiGejala(?p, ?g) ^ NyeriSaatMenggigit(?g) ^ dipicuOleh(?g, ?trig) ^ TekananSaatMenggigit(?trig) -> didugaMenderita(?p, Penyakit_Trauma_Oklusi)

12. p2_impaksi_molar_rule1
Pasien(?p) ^ mengalamiKondisi(?**p**, ?k1) ^ OperkulumBengkak(?k1) ^ mengalamiKondisi(?p, ?k2) ^ GigiErupsiSebagian(?k2) -> didugaMenderita(?p, Penyakit_Impaksi_Molar)

13. p2_impaksi_molar_rule2
Pasien(?p) ^ mengalamiGejala(?p, ?g) ^ Trismus(?g) ^ mengalamiKondisi(?p, ?k1) ^ GigiErupsiSebagian(?k1) ^ mengalamiKondisi(?p, ?k2) ^ PosisiMiring(?k2) -> didugaMenderita(?p, Penyakit_Impaksi_Molar)

14. p2_impaksi_molar_rule3
Pasien(?p) ^ mengalamiGejala(?p, ?g) ^ NyeriRahangBelakang(?g) ^ mengalamiKondisi(?p, ?k) ^ PosisiMiring(?k) -> didugaMenderita(?p, Penyakit_Impaksi_Molar)

15. p2_radiks_relikta
Pasien(?p) ^ mengalamiKondisi(?p, ?k1) ^ SisaAkar(?k1) ^ mengalamiKondisi(?p, ?k2) ^ GusiBenjol(?k2) -> didugaMenderita(?p, Penyakit_Radiks_Relikta)

16. p2_infeksi_pasca_cabut
Pasien(?p) ^ mengalamiKondisi(?p, ?k1) ^ RiwayatCabutGigi(?k1) ^ mengalamiKondisi(?p, ?k2) ^ LubangPascaCabut(?k2) ^ mengalamiGejala(?p, ?g) ^ NyeriHebat(?g) -> didugaMenderita(?p, Penyakit_Infeksi_Pasca_Cabut)

17. rekomendasi_spesialis_rule
Pasien(?p) ^ didugaMenderita(?p, ?penyakit) ^ membutuhkanSpesialis(?penyakit, ?spesialis) -> dirujukKe(?p, ?spesialis)