# KEGA Projekt - Laboratórium aplikovaných technológií umelej inteligencie

## Zameranie projektu
Projekt sa zameriava na vybudovanie moderného laboratória aplikovaných technológií umelej
inteligencie pre priemysel. Laboratórium bude pozostávať z 5 rôznych pracovísk zameraných na
spracovanie obrazu, videa a zvuku pre priemyselné aplikácie. Pracoviská sú navrhnuté tak, aby mohli
byť nezávislé od operačného systému (Linux, Windows) a softvéru pre HNS (Matlab, Python, ...).
Laboratórium budú využívať študenti 3. ročníka bakalárskeho štúdia a študenti 1. a 2. ročníka
inžinierskeho štúdia na vybraných predmetoch a študenti bakalárskych, diplomových, individuálnych
a tímových prác, ale aj doktorandi. Plánujeme nasledovné pracoviská:

## Pracovisko 5 - Spracovanie zvuku a iných signálov na detekciu anomálií metódami strojového učenia
Počítačová zostava, kvalitný mikrofón, Nvidia Jetson (Edge zariadenie), priemyselný
riadiaci systém. Cieľom pracoviska bude spracovanie zvuku a odoslanie výsledku spracovania do
priemyselného riadiaceho systému s cieľom učenia kvality.

### Detekcia anomálií v signálnych dátach metódami jednotriednej klasifikácie

Detekcia anomálií v signálnych dátach predstavuje významnú úlohu pri monitorovaní technických systémov, diagnostike porúch a identifikácii neštandardných prevádzkových stavov. 
Cieľom je automaticky rozpoznať odchýlky od normálneho správania systému na základe analýzy nameraných signálov, napríklad teploty, tlaku, vibrácií alebo elektrických veličín. 
Pri riešení tejto úlohy možno využiť **metódy jednotriednej klasifikácie (One-Class Classification)**, ktoré sa učia charakteristické vlastnosti normálnych dát bez potreby rozsiahlej množiny vzoriek reprezentujúcich poruchové stavy.

Medzi vhodné metódy patrí **One-Class SVM**, ktorá vytvára rozhodovaciu hranicu oddeľujúcu normálne vzorky od anomálií, **Isolation Forest**, ktorá identifikuje anomálie na základe ich jednoduchšej izolovateľnosti pomocou náhodných rozhodovacích stromov, 
a **autoenkóder (Autoencoder)**, ktorý sa učí rekonštruovať normálne signály a anomálie deteguje na základe zvýšenej chyby rekonštrukcie.

**Detekcia ochorenia z EKG signálu**
Experimentálne porovnanie metód bude realizované na verejne dostupnom datasete ECG5000, ktorý obsahuje elektrokardiografické signály s normálnymi aj abnormálnymi priebehmi. 
Modely budú trénované na normálnych vzorkách signálov a následne testované na dátach obsahujúcich normálne aj anomálne vzorky. 
Cieľom je porovnať schopnosť jednotlivých metód detegovať anomálie pomocou vhodných klasifikačných metrík, analyzovať vplyv nastavenia parametrov modelov a vyhodnotiť ich výpočtovú náročnosť.

Dataset ECG5000 je verejne dostupná množina elektrokardiografických (EKG) signálov pochádzajúcich z databázy BIDMC Congestive Heart Failure Database (PhysioNet). 
Obsahuje 5 000 vzoriek jednotlivých srdcových cyklov získaných zo záznamu pacienta so závažným srdcovým zlyhávaním. Každá vzorka predstavuje jeden srdcový cyklus, ktorý bol interpoláciou upravený na jednotnú dĺžku 140 hodnôt.
( [Dataset_ECG5000](https://www.kaggle.com/datasets/devavratatripathy/ecg-dataset/data) )

Literatúra a Dosiahnuté výsledky:
- Kajan, Detekcia anomálií - jednotriedna klasifikácia defektov, Prednáška HNS, FEI STU Bratislava, 2026, [Prezentacia_Detekcia_Anomalii_HNS_Kajan](document/Prezentacia_Detekcia_Anomalii_HNS_Kajan.pdf)

### Klasifikácia terénu zo signálov vibračných senzorov metódami strojového učenia  :
Automatické rozpoznávanie typu terénu predstavuje významnú úlohu v oblasti mobilnej robotiky, najmä pri autonómnej navigácii robotických systémov v neznámom alebo meniacom sa prostredí. 
Jedným z možných prístupov je využitie vibračných senzorov, ktoré zaznamenávajú mechanické vibrácie vznikajúce pri pohybe robota po rôznych typoch povrchov. 
Charakter týchto vibrácií závisí od vlastností terénu, ako sú jeho tvrdosť, drsnosť, nerovnosť či štruktúra. 
Analýzou nameraných signálov je možné identifikovať charakteristické príznaky umožňujúce rozlišovať jednotlivé typy povrchov, napríklad asfalt, betón, štrk, trávu alebo piesok.

Cieľom úlohy je navrhnúť a experimentálne overiť metódy strojového učenia na automatickú klasifikáciu typu terénu na základe signálov vibračných senzorov. 
Súčasťou riešenia bude predspracovanie nameraných signálov, extrakcia charakteristických príznakov v časovej a frekvenčnej oblasti a návrh klasifikačných modelov, napríklad SVM, Random Forest alebo viacvrstvových neurónových sietí (MLP). 
Alternatívnym prístupom je využitie hlbokých neurónových sietí, ktoré umožňujú automatickú extrakciu príznakov priamo zo signálov alebo ich časovo-frekvenčných reprezentácií. Použité budú CNN a LSTM siete. 
Jednotlivé metódy budú experimentálne porovnané z hľadiska úspešnosti klasifikácie a schopnosti rozlišovať rôzne typy terénu.

[Zadanie - Klasifikácia terénu pomocou SVM, MLP, LSTM a CNN](https://github.com/STU-FEI-OUI/HNS-test/blob/main/Zadania/HNS_Zadanie1.pdf)

Dataset a Programy k Zadaniu 1: [GoogleDisk - HNS/Cvicenia/Zadanie1](https://drive.google.com/drive/folders/11j4FFFKerQn-D_06xCKMpK6MajYdHAc3?usp=drive_link)

Literatúra:

[Peter Sarcevic - Online Outdoor Terrain Classification Algorithm ...](https://www.mdpi.com/2079-9292/12/15/3238)

[Ersek, Kajan, Korosi - Vibration based terrain classification...](https://reference-global.com/article/10.2478/jee-2025-0044)