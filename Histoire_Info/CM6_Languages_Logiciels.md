# Langages de Programmation

Plusieurs milliers de langages de programmation  
Chaines de bits => Assembleur => Haut niveau  
------------------------ 10 ans --------------------------->

## 1. Programmation de Haut niveau

Pour remedier aux limitations des premières machines :  
Programmation automatique [1949-1954]  
Speedcoding, A0 à A3, Laning Ziegler, ...  

- **Plankalkül** : affectation, conditions, while, logique mais notation très particulière

- **Fortran** : Language pour IBM 704, but : efficacité,  
proposé par John Backus, premier language de haut niveau  
=> Calcul à la portée des usagers
    - [1954] Soutient d'IBM
    - [1955] Début construction compilateur
    - [1957] compilateur (fabriquant du code efficace mais trop tolérant)
    - [1958] Fortran II
    - [1962] Fortran IV

- **Algol** : Language indépendant de la machine ?  
Tableaux dynamiques, structure en blocs, définitions rigoureuses  
Peu utilisé (IBM > All) mais influences ... -> Pascal ...
    - [1958] Création d'un commité, définition d'Algol 58
    - [1960] Rapport Algol 60, rôle important de Peter Naur
    - [1964] Cinquième compilateur donne lieu à une description très détaillée sur la conception d'un compilateur.

- **COBOL** : Pour applications de gestion    
Méprisé de la communauté académique
    - [1970] Devient le language le plus largement utilisé  
    80% des programmes existants sont écrits en COBOL !!

- **Lisp** : Language de manipulation de listes, basé sur l'appel de fonction  
=> Récurcivité, Le ramasse-miettes, Programmation Fonctionnelle ...

- **APL** : Structure & Operations sur Vecteurs, utilise des symboles spéciaux

## 2. Retour vers la machine

Faire un langage permettant d'être plus proche de la machine pour les OS et compilateurs.

- Assembleur déguisé :  
Visibilité des registres + conditions (if, while) + procédures

- La machine Virtuelle :  
Structure de donnée = mot, précurseur du C

## 3. Nouveaux Paradigmes

- **Languages à objets** : Modéliser le monde réel
    - [1967] Regrouper avec objets, classes, héritage
    - [1978] Métaclasses, polymorphisme
- **Languages logiques** : Modéliser le raisonnement
    - [1960] Déclaratif vs Procédural
    - [1972] Faits, Règles, moteur d'inférence

## 4. Qualités d'un langages de programmation

- **Bon Language ?** : Sûr, Rigoureux, Elegant/Lisible, Expressif, Efficace  


# Génie Logiciel

Ecrire des programmes corrects est difficile ...
Gros logiciels SABRE, SAGE, OS/360 (echec)

- [1960] **La crise du logiciel** : Nouvelle discipline
    - [1968] Première conférence : Problèmes => Composants réutilisables ?
    - [1969] Constat incompréhension entre théorie et pratique ...
- [1968 - 1975] **Les sept premières années**  
  => Design > Development > TEST > Maintenance  
  => Modèle de la cascade (rétro-actions) -> Retour Exp trop tard
  => Avancées théoriques, architecturales et méthodologique
    - [1967] Assertions
    - [1968] Influence de l'individu plus que les outils
    - [1969] Logique de Hoare (dehors)
    - [1976] Prédicats, méthode rigoureuse
    - [----] Conception descendante, décomposition en modules, interface
