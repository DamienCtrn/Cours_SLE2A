# Industrie informatique : du mainframe au mini #

## Partie 1 #
**Technos :**  
Tores de Ferrite > Transistors > Circuits Intégrés > LSI > VLSI > ...  
**Utilisation majoritaire :**  
Mainframe > Mini-ordinateurs, Supercalculateurs > Ordinateurs personnels > Machines parallèles
**Entreprises :**  
IBM >>> le BUNCH, Hewlett Packard

#### 1. En France #
- [1966] **Plan Calcul** : Doter la France de moyens de Gestion :  
    - Fusion de la SEA et CAE : CII
    - Concoit Iris 50 et 80 (SDS Sigma 7 en plus gros)
- [1976] Section Informatique au CNRS
- [1982] Informatique au CNU
- [2003] Informatique à l'académie des sciences

#### 2. Nouveautés Technologiques #
- [1953] Tores de ferrite par *Whirlwind*  
  (1-2 mm), 2 états stables, changement avec courant elec
- [1957] Transistors (remplacent tubes à vide)
- [19__] Circuits Intégrés

#### 3. Nouveautés architecturales #
- [19__] Unité Virgule flottante
- [1956] Interruptions
- [1957] Canaux d'entrée-sortie
- [1968] Cache

#### 4. Batailles Industrielles #
- [1951-1955] IBM vs UNIVAC
- [1955-1960] IBM et les 7 nains

#### 5. Machines Notables
- {IBM 1401} : petite machine de gestion  
    (gros succès, pas très cher, imprimante très rapide)
- {IBM 360} : Pari pour la portabilité des programmes  
    - Microprogrammation (émulations des modèles anciens)
    - Solid Logic Technology (diodes et transistors encapsulés dans verre)
    - Architecture unique & simple (mots 32 bits)  

**Mini-ordinateurs :**  
mot de mem courts, pas encombrement, coût réduit, proche des utilisateurs  
- {PDP-11} mots 16 bits, 8 registres, bus unique, bcp Interruptions, DMA  
    => 600k exemplaires vendus de 1970 à 1990
- {MAT-01} calculateur industriel developpé à Grenoble au labo d'automatique  
    mais le Plan Calcul détruit les retombées ...

#### 6. Les Usages de l'informatique #
- [1955-1960] Mécanographie -> Informatique
- [1960-1970] Gestion, Banque, Finance, Science, Temps réel  
    => Croissance de l'importance du logiciel

## Partie 2 #
Transistors (1955) -> CI (1965) -> u-Processeurs (1971)

#### 1. Transistor into Circuits Intégrés #
Division Fairchild Semiconductor --> Démarage de la Silicon Valley  
Premier CI au Germanium en 1958 puis au Silicium pour avoir des couches
- [1968] Création d'Intel -> première mémoire SRAM 256 bits avec MOSFET
- [1971] Premier u-Processeur : Intel 4004  
    2300 transitors, 740kHz, 16 registres, 46 instructions  
- [1973] Premier u-Ordinateur : Micral-N avec Intel 8008

#### 2. Premiers ordinateurs persos #
Initialement, public : radio amateurs
- [1974] Premier ordinateur en kit ($400), dev de BASIC par Microsoft
- [1975-1977] Essor des ordinateurs personnels -> Apple
- [1977] Apple II : Ordinateur monté pour le grand public ($1200)  
- RadioShack (par Tandy) ($600)
- [1977] DEC VAX

#### 3. Role clé du logiciel #
Sur Apple II (1977) par expl:
- VisiCalc : Tableur !!
- WYSIWYG WordStar : Traitement de texte !
- Jeux

#### 4. La nouvelle stratégie d'IBM #
Fin du Mainframe -> Sous-traitance, Specs ouvertes  
IBM comme DEC se sont laissés surprendre par les avancées technologiques

**Processeurs 32 bits + Graphique + Unix + Réseaux = Stations de Travail**

## Partie 3 : Parallèlisation #

#### 1. Les premiers Supercalculateurs #
- [1956-1961] IBM 7030 : 0.3 MFlops
- [1962-1964] CDC 6600 : 1 MFlops
- [1966-1969] IBM 360/-- : 4 MFlops
- [1965] Illiac IV : 100 MFlops
- [1976] Cray-1 : 130 MFlops

#### 2. Le pipelinage qui se rapporte au plumage #
En RISC : FETCH > DEC > EXEC > MEM > WRITE + Pipeline => 3x plus vite ?  
**Mais** Aléas => Stall / Bypass / Ordonnancement des instructions ...

#### 3. Architectures superscalaires #
Lancer plusieurs instructions à la fois sur plusieurs Machines
**Mais** Nécessité de pouvoir parallèliser les instructions !

\+ Machines Vectorielles ....
