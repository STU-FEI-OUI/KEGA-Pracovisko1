# KEGA Projekt - Laboratórium aplikovaných technológií umelej inteligencie

## Zameranie projektu
Projekt sa zameriava na vybudovanie moderného laboratória aplikovaných technológií umelej
inteligencie pre priemysel. Laboratórium bude pozostávať z 5 rôznych pracovísk zameraných na
spracovanie obrazu, videa a zvuku pre priemyselné aplikácie. Pracoviská sú navrhnuté tak, aby mohli
byť nezávislé od operačného systému (Linux, Windows) a softvéru pre HNS (Matlab, Python, ...).
Laboratórium budú využívať študenti 3. ročníka bakalárskeho štúdia a študenti 1. a 2. ročníka
inžinierskeho štúdia na vybraných predmetoch a študenti bakalárskych, diplomových, individuálnych
a tímových prác, ale aj doktorandi. Plánujeme nasledovné pracoviská:

## Pracovisko 1 - Kontrola kvality výrobkov pomocou hlbokých neurónových sietí
Počítačová zostava s výkonnou grafickou kartou, kvalitná hĺbková kamera, priemyselný riadiaci systém, model. 
Cieľom pracoviska bude spracovanie obrazu na kontrolu kvality objektov (výrobkov).

### Klasifikácia defektov zvarov pomocou hlbokých neurónových sietí.
**Klasifikácia defektov zvarov pomocou vizuálnej kontroly**

Kontrola kvality zvarových spojov predstavuje dôležitú súčasť zabezpečenia spoľahlivosti a bezpečnosti zváraných konštrukcií. 
Automatizovaná vizuálna kontrola s využitím priemyselných kamier a laserových skenerov umožňuje bezkontaktné získavanie informácií o povrchu zvarov a identifikáciu rôznych typov defektov, ako sú trhliny, pórovitosť, zápaly, prevýšenie či nepravidelná geometria zvaru.
Kamerové systémy poskytujú dvojrozmerné obrazy zachytávajúce vzhľad a povrchové charakteristiky zvaru, zatiaľ čo laserové skenery umožňujú získavať trojrozmerné údaje o jeho geometrii a povrchových nerovnostiach. 
Na automatickú detekciu a klasifikáciu defektov možno využiť metódy spracovania obrazu a hlbokého učenia, predovšetkým konvolučné neurónové siete (CNN). 
Kombinácia obrazových a geometrických údajov vytvára predpoklady na zvýšenie spoľahlivosti rozpoznávania defektov a umožňuje objektívne hodnotenie kvality zvarových spojov v priemyselných podmienkach. 
Na obrázku je znázornený princíp klasifikácie defektov zvarov pomocou CNN, kde obraz z kamery vstupuje do CNN, ktorá z obrazu získa príznaky potrebné na binárnu klasifikáciu Defekt/Bez defektu alebo viactriednu, kde sa určí aj typ defektu.
![princip weld defect](image/klasifikacia_weld_defekt_princip.png)
Obr.1 Principiálna schéma klasifikácie defektov zvarov pomocou CNN

#### Dataset - Kontrola kvality zvarov z kamery – 4 skupiny (Ok, 2025-kráterový lunker, 510-diera, 500-poškodený povrch zvaru):
[Weld_Defect_Camera_Dataset](https://drive.google.com/drive/folders/1SUivIX-uDGs74XNegNQp95wvQ78C5DIe?usp=drive_link)

Dataset - Kontrola kvality zvarov z laserového skenera – 2 skupiny (binárna klasifikácia Good/Bad Weld):
[Weld_Defect_Laser_Dataset](https://drive.google.com/drive/folders/1dyKmhW-oL_biiiVoooNsTCJpm8OgUhDl?usp=drive_link)


Dosiahnuté výsledky:
- Švec, Klasifikácia defektov robotmi realizovanými zvarmi AI nástrojom, DP FEI STU Bratislava, 2024, [Prezentacia_DP_Svec_Klasifikacia_defektov_zvarov_kamera](document/Prezentacia_DP_Svec_Klasifikacia_defektov_zvarov.pdf)

- Adam, Detekcia defektov zvarov pomocou hlbokých neurónových sietí, DP FEI STU Bratislava, 2025, [Prezentacia_DP_Adam_Klasifikacia_defektov_zvarov_laser](document/Prezentacia_DP_Adam_Klasifikacia_defektov_zvarov.pdf)

- Palček, Vizuálna kontrola zvarov pomocou hlbokých neurónových sietí, DP FEI STU Bratislava, 2026, [Prezentacia_DP_Palcek_Klasifikacia_defektov_zvarov_plechov](document/Prezentacia_DP_Palcek_Klasifikacia_defektov_zvarov.pdf)

Literatúra:
- S. Kajan, M. Trebuľa, F. Duchoň, Z. Kovaríková, M. Švolík and D. Švec, "Robotic Vision Inspection of Weld Quality Using Convolutional Neural Networks," 2024 25th International Carpathian Control Conference (ICCC), Krynica Zdrój, Poland, 2024, pp. 01-05, doi: 10.1109/ICCC62069.2024.10569157. [Kajan_kol_Weld_Visual_Inspection](https://ieeexplore.ieee.org/document/10569157)

- S. Kajan, M. Trebuľa, F. Duchoň, Z. Kovaríková, M. Kováč and J. Pavlovičová, "Weld Defect Recognition and Detection from Video Using Deep Learning Methods," 2025 Cybernetics & Informatics (K&I), Mikulov na Morave, Czech Republic, 2025, pp. 1-5, doi: 10.1109/KI64036.2025.10916449. [Kajan_kol_Weld_Defect_Recognition](https://ieeexplore.ieee.org/document/10916449)

- S. Kajan, M. Trebuľa, "Robotická vizuálna kontrola zvarov využitím metód hlbokého učenia," ATP Journal júl 2025. [Kajan_Trebula_Weld_Defect_ATP](https://www.atpjournal.sk/rubriky/prehladove-clanky/roboticka-vizualna-kontrola-zvarov-vyuzitim-metod-hlbokeho-ucenia.html?page_id=42144)

### Detekcia defektov výrobkov pomocou autoenkóderov a FCDD hlbokých neurónových sietí.
**Detekcia defektov výrobkov (casting dataset) pomocou Autoenkódera a FCDD**

Automatická vizuálna kontrola kvality výrobkov predstavuje významnú oblasť využitia metód umelej inteligencie v priemyselnej výrobe. 
Jednou z dôležitých úloh je identifikácia defektných výrobkov na základe analýzy ich obrazových údajov. 
Pri riešení tejto úlohy sa čoraz častejšie využívajú metódy hlbokého učenia zamerané na detekciu anomálií, ktoré umožňujú rozpoznávať defekty aj bez potreby rozsiahlych množín označených obrazov chybných výrobkov.

Cieľom úlohy je navrhnúť a experimentálne porovnať metódy klasifikácie defektných a bezchybných výrobkov založené na **autoenkóderoch (AE)** a **hlbokých neurónových sieťach FCDD (Fully Convolutional Data Description)**. 
Autoenkódery využívajú princíp rekonštrukcie vstupného obrazu, pričom odchýlky medzi pôvodným a rekonštruovaným obrazom môžu indikovať prítomnosť defektov. 
Metóda FCDD je založená na učení príznakovej reprezentácie obrazov a umožňuje identifikovať anomálne oblasti prostredníctvom priestorových máp anomálií.
Na experimentálne overenie navrhnutých riešení bude použitý verejne dostupný **dataset Casting**, ktorý obsahuje obrazy bezchybných a defektných kovových odliatkov. 
Súčasťou riešenia bude predspracovanie obrazových údajov, návrh a trénovanie neurónových modelov, optimalizácia ich parametrov a vyhodnotenie dosiahnutých výsledkov pomocou vhodných klasifikačných metrík. 
Osobitná pozornosť bude venovaná porovnaniu úspešnosti klasifikácie jednotlivých metód a možnostiam lokalizácie defektov na povrchu výrobkov vizualizačnými technikami Grad-CAM.

![struktura autoenkoder](image/autoenkoder_defekt_princip.png)
Obr.2 Architektúra autoenkódera na detekciu defektov

![struktura FCDD](image/FCDD_defekt_princip.png)
Obr.3 Architektúra FCDD na detekciu defektov

#### Casting Dataset - obrazy bezchybných a defektných kovových odliatkov – binárna klasifikácia:
[Casting_Dataset_Drive](https://drive.google.com/drive/folders/1pNCrX0CoxX2uKjdOMzKOOCkc1X3u8WQc?usp=drive_link) , 
[Casting_Dataset_Kaggle](https://www.kaggle.com/datasets/ravirajsinh45/real-life-industrial-dataset-of-casting-product)

Dosiahnuté výsledky:
- Palček, Vizuálna kontrola zvarov pomocou hlbokých neurónových sietí, DP FEI STU Bratislava, 2026, [Prezentacia_SVOC_Palcek_Detekcia_defektov](document/Prezentacia_SVOC_Palcek_Detekcia_defektov.pdf)

Literatúra:
- Palček, Kajan, "Experimentálne porovnanie metód hlbokého učenia pre vizuálnu inšpekciu defektov," ŠVOČ, FEI STU Bratislava, 2026, [Palcek_Kajan_SVOC](document/Palcek_SVOC.pdf)

- J.K. Chow, Z. Su, J. Wu, P.S. Tan, X. Mao, Y.H. Wang.,Anomaly detection of defects on concrete structures with
the convolutional autoencoder. ScienceDirect - Advanced Engineering Informatics, Volume 45:4–5 str., August 2020, [Anomaly_detection_defects_autoenkoder](https://www.sciencedirect.com/science/article/pii/S1474034620300744)

- P. Liznerski, L. Ruff, R. A. Vandermeulen, B. J. Franks, M. Kloft, and K.-R. Müller. Explainable deep one-class
classification. Preprint arXiv:2007.01760, Marec 18, 2021. [Anomaly_detection_defects_FCDD](https://arxiv.org/abs/2007.01760)

- L. Ruff, R. A. Vandermeulen, B. J. Franks, K.-R. Müller, and M. Kloft. Rethinking assumptions in deep anomaly
detection. Preprint arXiv:2006.00339, Máj 30, 2020. [Anomaly_detection_defects_2](https://arxiv.org/abs/2006.00339)

- K. Simonyan and A. Zisserman. Very deep convolutional networks for large-scale image recognition. Preprint
arXiv:1409.1556, April 10, 2015. [Anomaly_detection_defects_3](https://arxiv.org/abs/1409.1556)

### Praktické príklady klasifikácie defektov pomocou CNN.
**Praktické príklady defektov - jamy na ceste, defekty na pneumatikách, detekcia požiaru**

V praxi sa veľmi často stretávame s riešením úloh detekcie defektných (anomálnych) stavov. Na príkladoch ako sú jamy na ceste, defekty na pneumatikách, detekcia požiaru si overíme schopnosť CNN riešiť problematiku detekcie defektov.  
Cieľom úlohy je navrhnúť a experimentálne porovnať rôzne štruktúry CNN alebo Vizuálnych transformerov (ViT) pre rôzne úlohy klasifikácie defektov.
Na experimentálne overenie navrhnutých riešení budú použité verejne dostupné datasety. 
Súčasťou riešenia bude predspracovanie obrazových údajov, návrh a trénovanie neurónových modelov, optimalizácia ich parametrov a vyhodnotenie dosiahnutých výsledkov pomocou vhodných klasifikačných metrík. 
Osobitná pozornosť bude venovaná porovnaniu úspešnosti klasifikácie jednotlivých modelov a možnostiam lokalizácie defektov na obraze vizualizačnými technikami Grad-CAM.

#### Datasety detekcia defektov - jamy na ceste, defekty na pneumatikách, detekcia požiaru:
[Jamy_cesta_Dataset_Drive](https://drive.google.com/drive/folders/1d3atNCQK9POrsjQJiVZ6M8HoPEfCaTn6?usp=drive_link) 

[Pneumatiky_Dataset_Drive](https://drive.google.com/drive/folders/1EO9dj8x2OM21ZSBs8xlqTLSzH-FDLOBB?usp=drive_link)

[Poziar_Dataset_Kaggle](https://www.kaggle.com/datasets/amerzishminha/forest-fire-smoke-and-non-fire-image-dataset)

Dosiahnuté výsledky:
- Mihálik, Tinák, Rozpoznávanie jám na ceste, Projekt HNS, 2025, [Vysledky_HNS_Projekt_Mihalik_Tinak](document/Prezentacia_HNS_Projekt_Detekcia_jam_Mihalik_Tinak.pdf)

- Piwková, Práznovský, Rozpoznávanie defektov na pneumatikách, Projekt HNS, 2025, [Vysledky_HNS_Projekt_Piwkova_Praznovsky](document/Prezentacia_HNS_Projekt_Detekcia_pneumatiky_Piwkova_Praznovsky.pdf)


**Priemyselné datasety**
Dataset povrchových defektov oceľového pásu  – NEU Surface defect Dataset
Klasifikácia defektov oceľového plechu, 6 skupín (valcované okuje (RS), škvrny (Pa), praskliny (Cr), jamkovitý povrch (PS), inklúzie (In) a škrabance (Sc))
( [Dataset_NEU_DET](https://www.kaggle.com/datasets/rdsunday/neu-urface-defect-database) )

Magnetic Tile Defect Dataset
Dataset na namierený na kontrolu kvality produktov v továrňach na magnetické dlaždice v provincii Zhejiang v Číne, najväčšej výrobnej základni magnetických dlaždíc na svete. 
Na zmiernenie ľudskej práce bolo navrhnutých mnoho techník spracovania obrazu, ktoré sa pokúšajú o vykonanie takýchto kontrolných úloh. 
Pri automatickej detekcii poškodenia magnetických dlaždíc sa vyskytlo niekoľko úzkych miest, vrátane zložitosti textúry, rozmanitosti tvarov defektov a náhodnosti svetelných podmienok na magnetických dlaždiciach. 
Cieľové defekty sú praskliny, zlomy a strapce.
( [Dataset_Magnetic_Tile](https://www.kaggle.com/datasets/alex000kim/magnetic-tile-surface-defects) )

GC10-DET - Metallic Surface Defect Detection
Detekcia defektov kovových povrchov je nevyhnutný a nevyhnutný proces na kontrolu kvality priemyselných výrobkov. 
Vzhľadom na obmedzený rozsah údajov a kategórie defektov však existujúce súbory údajov o defektoch vo všeobecnosti nie sú k dispozícii na nasadenie detekčného modelu. 
Na riešenie tohto problému prispievame novým súborom údajov s názvom GC10-DET na detekciu defektov kovových povrchov vo veľkom meradle. 
Súbor údajov GC10-DET má veľké výzvy, pokiaľ ide o kategórie defektov, počet obrázkov a rozsah údajov. 
( [Dataset_GC10_DET](https://www.kaggle.com/datasets/alex000kim/gc10det/data) )

AL10-DET (Aluminum 10 Defect Detection Dataset) 
je dataset určený na detekciu povrchových defektov hliníkových profilov pomocou metód objektovej detekcie.
AL10-DET obsahuje snímky povrchu extrudovaných hliníkových profilov získané v priemyselných výrobných podmienkach.
( [Dataset_AL10_DET](https://www.kaggle.com/datasets/arcanine9/al10-det/data) )

Dosiahnuté výsledky:
- Szépvölgyi, Porovnanie detektorov na priemyselných datasetov, Projekt HNS, 2025, [Vysledky_HNS_Projekt_Szépvölgyi](document/Prezentacia_Szepvolgyi_Porovnanie_detektorov.pdf)

#### Dataset detekcia defektov na podložkách - 4 typy defektov (jamka - circular_cavity, šrabanec - scratch, zárez – burr, prevýšenie materiálu - excess_material):
[Klasifikacia_defekty_Podložky](https://drive.google.com/drive/folders/1PVE357M-8uburXtl5kFwjo_nowSup1Xx?usp=drive_link)

Detekcia defektov pomocou YOLO detektora

[Detekcia_defekty_Podložky](https://drive.google.com/drive/folders/1QcswFcZ1FPBEZM2TyV8x0bvTimcJgAfQ?usp=drive_link)

[Detekcia_defekty_Podložky_Roboflow](https://universe.roboflow.com/hemorrhagesegmentation/tp26_detection)

### Detekcia anomálií - signálne data - jedno triedna klasifikácia iba z normálnych dát.
**Detekcia ochorenia z EKG signálu**

### Detekcia anomálií v signálnych dátach metódami jednotriednej klasifikácie

Detekcia anomálií v signálnych dátach predstavuje významnú úlohu pri monitorovaní technických systémov, diagnostike porúch a identifikácii neštandardných prevádzkových stavov. 
Cieľom je automaticky rozpoznať odchýlky od normálneho správania systému na základe analýzy nameraných signálov, napríklad teploty, tlaku, vibrácií alebo elektrických veličín. 
Pri riešení tejto úlohy možno využiť **metódy jednotriednej klasifikácie (One-Class Classification)**, ktoré sa učia charakteristické vlastnosti normálnych dát bez potreby rozsiahlej množiny vzoriek reprezentujúcich poruchové stavy.

Medzi vhodné metódy patrí **One-Class SVM**, ktorá vytvára rozhodovaciu hranicu oddeľujúcu normálne vzorky od anomálií, **Isolation Forest**, ktorá identifikuje anomálie na základe ich jednoduchšej izolovateľnosti pomocou náhodných rozhodovacích stromov, 
a **autoenkóder (Autoencoder)**, ktorý sa učí rekonštruovať normálne signály a anomálie deteguje na základe zvýšenej chyby rekonštrukcie.

Experimentálne porovnanie metód bude realizované na verejne dostupnom datasete ECG5000, ktorý obsahuje elektrokardiografické signály s normálnymi aj abnormálnymi priebehmi. 
Modely budú trénované na normálnych vzorkách signálov a následne testované na dátach obsahujúcich normálne aj anomálne vzorky. 
Cieľom je porovnať schopnosť jednotlivých metód detegovať anomálie pomocou vhodných klasifikačných metrík, analyzovať vplyv nastavenia parametrov modelov a vyhodnotiť ich výpočtovú náročnosť.

Dataset ECG5000 je verejne dostupná množina elektrokardiografických (EKG) signálov pochádzajúcich z databázy BIDMC Congestive Heart Failure Database (PhysioNet). 
Obsahuje 5 000 vzoriek jednotlivých srdcových cyklov získaných zo záznamu pacienta so závažným srdcovým zlyhávaním. Každá vzorka predstavuje jeden srdcový cyklus, ktorý bol interpoláciou upravený na jednotnú dĺžku 140 hodnôt.
( [Dataset_ECG5000](https://www.kaggle.com/datasets/devavratatripathy/ecg-dataset/data) )

