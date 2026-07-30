# Obrázky ku kazuistikám — náročná sada, 31 prípadov

Aktualizované 30. júla 2026. Pôvodných 30 ľahkých kazuistík (infarkt myokardu, apendicitída,
komunitná pneumónia, DKA, CMP a podobne) je nahradených sadou 31 náročných prípadov typu
„klasická zebra". Obrázky k starým prípadom sú v `_stare-pripady/` — v hre sa už nepoužívajú
a ich čísla NEODPOVEDAJÚ novému poradiu.

Ku každému prípadu je v `index.html` pri príslušnej indícii pole `imageHint` s presným
anglickým zadaním pre AMBOSS. Nižšie je prehľad vrátane toho, na ktorej indícii obrázok visí.

## Prehľad zadaní

| č. | diagnóza | indícia | čo musí obrázok ukazovať (zadanie pre AMBOSS) |
|---|---|---|---|
| 01 | Akútna intermitentná porfýria | 5 | port wine-colored / dark reddish-brown urine sample in acute intermittent porphyria |
| 02 | Hypertrofická kardiomyopatia | 5 | echocardiogram in hypertrophic cardiomyopathy — asymmetric septal thickening with systolic anterior motion of the mitral valve and left ventricular outflow tract obstruction |
| 03 | Celiakia | 5 | duodenal biopsy in celiac disease — villous atrophy, crypt hyperplasia and intraepithelial lymphocytosis |
| 04 | Alportov syndróm | 5 | electron microscopy in Alport syndrome — irregular thinning and thickening with longitudinal splitting of the glomerular basement membrane (basket-weave appearance) |
| 05 | Skleróza multiplex | 5 | brain MRI in multiple sclerosis — multiple periventricular T2 hyperintense demyelinating plaques (Dawson fingers) |
| 06 | Karcinoidový syndróm | 5 | carcinoid tumor histology — nests of neuroendocrine cells forming rosettes, chromogranin A positive |
| 07 | Hereditárna sferocytóza | 5 | peripheral blood smear in hereditary spherocytosis — small round RBCs without central pallor |
| 08 | Sarkoidóza | 5 | chest imaging in sarcoidosis — bilateral hilar lymphadenopathy |
| 09 | Wilsonova choroba | 5 | Kayser-Fleischer ring — golden-brown copper deposit at corneal limbus (Descemet membrane), slit-lamp photo |
| 10 | Feochromocytóm | 5 | adrenal mass on abdominal CT in pheochromocytoma |
| 11 | Achalázia | 4 | barium swallow in achalasia — dilated esophagus with smooth tapering distal stenosis (bird's beak sign) |
| 12 | Dermatomyozitída | 5 | Gottron papules over the extensor surfaces of the finger joints in dermatomyositis (and heliotrope eyelid edema) |
| 13 | IgA nefropatia | 5 | renal biopsy immunofluorescence in IgA nephropathy (Berger disease) — granular mesangial IgA immune complex deposits |
| 14 | Lambertov-Eatonov myastenický syndróm | 5 | repetitive nerve stimulation in Lambert-Eaton myasthenic syndrome — low baseline CMAP amplitude with marked incremental response at high-frequency stimulation or post-exercise |
| 15 | Primárna biliárna cholangitída | 5 | liver histology in primary biliary cholangitis — lymphocytic destruction of small intrahepatic bile ducts with granulomatous florid duct lesion |
| 16 | Deficiencia G6PD | 5 | peripheral blood smear in G6PD deficiency — Heinz bodies and bite cells |
| 17 | Primárny hyperaldosteronizmus | 5 | adrenal CT showing a unilateral adrenal adenoma (Conn syndrome) in primary hyperaldosteronism |
| 18 | Granulomatóza s polyangiitídou | 5 | chest CT in granulomatosis with polyangiitis — multiple bilateral pulmonary nodules with central cavitation |
| 19 | Whippleova choroba | 5 | duodenal biopsy in Whipple disease — PAS-positive foamy macrophages in the intestinal lamina propria |
| 20 | Huntingtonova choroba | 5 | brain MRI in Huntington disease — atrophy of the caudate and putamen with ex vacuo ventriculomegaly |
| 21 | Polycytémia vera | 5 | erythromelalgia — severe burning pain with red-blue discoloration of the extremities in polycythemia vera |
| 22 | Deficiencia alfa-1-antitrypsínu | 5 | chest CT showing panacinar emphysema in alpha-1 antitrypsin deficiency |
| 23 | Antifosfolipidový syndróm | 5 | livedo reticularis — net-like reticular violaceous skin mottling (antiphospholipid syndrome) |
| 24 | Akromegália | 5 | acromegaly — coarsened facial features with prognathism and enlarged hands (soft tissue overgrowth) |
| 25 | Neuroblastóm | 5 | neuroblastoma histology — Homer-Wright rosettes (neuroblasts surrounding a central area of neuropil) |
| 26 | Trombotická trombocytopenická purpura | 4 | peripheral blood smear in thrombotic thrombocytopenic purpura — schistocytes (fragmented RBCs) of microangiopathic hemolytic anemia |
| 27 | Hemochromatóza | 5 | liver biopsy with Prussian blue stain showing hemosiderin (iron) deposition in hereditary hemochromatosis |
| 28 | Wernickeho encefalopatia | 5 | brain MRI in Wernicke encephalopathy — symmetric FLAIR hyperintensities in the mammillary bodies and periaqueductal region |
| 29 | Paroxyzmálna nočná hemoglobinúria | 6 | flow cytometry in paroxysmal nocturnal hemoglobinuria — CD55 (DAF) and CD59 (MIRL) deficient granulocyte/erythrocyte population, GPI-anchor negative clone |
| 30 | Addisonova choroba | 5 | hyperpigmentation of buccal mucosa and palmar creases in primary adrenal insufficiency (Addison disease) |
| 31 | Otrava olovom | 5 | peripheral blood smear in lead poisoning — basophilic stippling of erythrocytes |

## Poradie odhaľovania

Číslo indície je hodnota `specificity`, nie pozícia v poli. Obrázok je vždy až na 4. až 6.
indícii — na 1. až 3. by prípad prezradil.

## Pripomienka k textu

Ak indícia dostane pole `image`, obrázok **nahradí** text indície. Text pri takej indícii
je preto len krátky popisok („Echokardiografia, parasternálna dlhá os.") a samotný
diagnostický nález sa nikdy nepíše do textu — inak by obrázok stratil zmysel.

## AMBOSS články

Odkazy sa vedú v `amboss-links.csv` v koreňovom priečinku. Pre novú sadu je zatiaľ
všetkých 31 riadkov prázdnych (`overene = nie`).
