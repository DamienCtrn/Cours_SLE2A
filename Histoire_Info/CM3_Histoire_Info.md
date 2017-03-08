# Les premiers ordinateurs à mémoire programmée #

#### 1. Problème de la mémoire #
3 Possibilités :
 - Flip-Flop (Colossus, peut adaptés a grande mem)
 - **Ligne à retard**  
 Circulation d'ondes de pression dans un tube de mercure  
 Utilisation de capteurs piezos  
 => Necessité horloge très précise  
 => Lecture Sequentielle (attente)  
 Utilisé dans EDVAC, UNIVAC, ACE (de Turing)
 - Tube cathodique (Tableau de charges électriques)

#### 2. ENIAC -> UNIVAC #
Eckert et Mauchly créent ECC (startup) pour créer UNIVAC  
Survie difficile (argent et délai) => Achat par Remington Rand  
[1951] : Livraison UNIVAC  
 - Sa mémoire : 1000 mots de 12 caractères, tps d'accès 222 us  
 - Entrée/Sortie : 10 unités de bandes magnétiques 7200 car/s  
 - Programmation : Instruction presque assemblage à 1 adresse
puis utilisation sous-programmes et édition de liens

**=> Cartes perforées >> Bandes magnétiques**  
**=> Début Programmation**

#### 3. Les Inventions Anglaises #
 - **Maurice Wilkes** [PhD Physique : ondes radios]  
 Concoit et réalise EDSAC (cherche sécurité), Microprogrammation
 - **David Wheeler**  
 Notion de sous-programmes (appel et retour, paramètres)
 - **WWG** [Livre de programmation de l'EDSAC]  
 Microprogrammation, Mise au point Interprétative
 - **Max Newman** [Mathématicien]  
 Crée le département d'informatique
 - **Le tube Williams**  
 1 bit = 1 charge électrique sur le fond d'un tube cathodique (512 à 1024)  
 Lecture non-séquentielle mais destructive -> regénérer la charges  
 - **[1948] Manchester Baby**  
 Réalisation rapide d'un mémoire avec un tube Williams  
 Insertion manuelle bit par bit (1024 en tout)  
 Donne le Mark-1 en version améliorée  
 - **l'ACE** [par Turing]  
 fait Pilot ACE : version réduite au final  
 -> Programmation : [src -> dest, instruction suiv] laborieuse mais optimisée
 - **IAS**  
 Bonne documentation de conception & architecture -> Héritage
 - **Whirlwind** [Simulateur de vol]  
 -> Problème mémoire : Résolution avec **Tores de ferrites** (grande avancée en terme de mémoire)

#### 4. Situation en 1951 #
 - Marché s'ouvre au traitement de données
 - Seuil du développement industriel
 - Conception dans les universités régresse
 - Logiciel va devenir critique
