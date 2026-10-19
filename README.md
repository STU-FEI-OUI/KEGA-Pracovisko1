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
Obr.5 Principiálna schéma klasifikácie defektov zvarov pomocou CNN

#### Dataset - Kontrola kvality zvarov z kamery – 4 skupiny (Ok, 2025-kráterový lunker, 510-diera, 500-poškodený povrch zvaru):
[Weld_Defect_Dataset](https://drive.google.com/drive/folders/1SUivIX-uDGs74XNegNQp95wvQ78C5DIe?usp=drive_link)

Dosiahnuté výsledky:
- Švec, Klasifikácia defektov robotmi realizovanými zvarmi AI nástrojom, DP FEI STU Bratislava, 2024, [Prezentacia_DP_Svec_Klasifikacia_defektov](document/Prezentacia_DP_Svec_Klasifikacia_defektov_zvarov.pdf)

Literatúra:
- S. Kajan, M. Trebul'a, F. Duchoň, Z. Kovaríková, M. Švolík and D. Švec, "Robotic Vision Inspection of Weld Quality Using Convolutional Neural Networks," 2024 25th International Carpathian Control Conference (ICCC), Krynica Zdrój, Poland, 2024, pp. 01-05, doi: 10.1109/ICCC62069.2024.10569157. [Kajan_kol_Weld_Visual_Inspection](https://ieeexplore.ieee.org/document/10569157)

- S. Kajan, M. Trebul’a, F. Duchoň, Z. Kovaríková, M. Kováč and J. Pavlovičová, "Weld Defect Recognition and Detection from Video Using Deep Learning Methods," 2025 Cybernetics & Informatics (K&I), Mikulov na Morave, Czech Republic, 2025, pp. 1-5, doi: 10.1109/KI64036.2025.10916449. [Kajan_kol_Weld_Defect_Recognition](https://ieeexplore.ieee.org/document/10916449)


