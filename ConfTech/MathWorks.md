# MathWorks
*Polyspace Code Prover - Bug Finder*
**Abstract Interpretation in a Commercial Tool**
-> Dev ici et utilisé dans le monde entier maintenant

Olivier Bouissou (Ancien Prof)

=> **Maths vers Commercial ?**

Plan:
- MathWorks
- Interprétation Abstraite
- Technical challenges
- Technological challenges

## MathWorks
=> **\$ \$ \$** *~ 1Milliard revenu annuel*
=> *~ 4000 employés*
=> *90 produits, 12 langages prog, codes vieux de 32 ans ...*
=> **MATHS + DEV SOFT DE QUALITAIENT**

*Produits* :
- MatLab (au départ calcul matriciel - 1985)
- Simulink (modelisation systemes, pratique - 1990)
- D'autres outils (génération code, vérification code)
=> **Polyspace**:
    - Racheté par MathWorks en 2007
    - 40 ingés à Grenoble + Paris
    - Utilisé en Aérospatial, Défence, Automobile, Médical = **Embarqué**

## Interprétation Abstraite

#### Goal ?
Méthode automatique pour ***prouver*** qu'il n'y a pas d'erreur dans un programme
=> **Press Button**
=> **Répondre je ne sais pas dans le moins de cas possible**

#### Bug ? Erreur ?
- Division par 0 sur var non initialisée, Overflow d'entier
- Accès case mem non allouée
- Variable locale, Pointeurs non initialisée
- Code Inateignable
- Boucles, fonction ne terminant jamais
=> **Ensemble constructions qui font que le prog s'arrête ou n'est pas bien défini**

*Exemples*
- Ariane 5 : Overflow
- Missiles Patriot : Float générant petite erreur à la longue
- Panne de Courant : Concurrance accès mem + propagation erreurs

#### Prouver absences erreurs ?
*Exemple :* Calculer le signe à la place de la valeur
=> **Prouver pour sous-ensemble**

## Technical Challenges

#### Difficulté des Pointeurs
- Déréférencement dans endroit foireux, null ...
- Mais peu de connaissances sur interfaçages => **Hypothèses**
- Flots de controles + Valeurs + Pointeurs ... => **Compliqué**

=> **Algo pour prouver pointeurs**:
- Pour chaque pointeur on regarde sur quelle var/zone il peut pointer
- Différent critères :
    - Sensibles aux **flots de controles** = Etats pour chaque lignes de codes
    - Non sensible = Tout Etats éventuellement atteignable
    - Sensibles aux **appels (fcts)** = Etats pour chaque lignes de codes
    - Non sensible = Globale
- **[Andersen]** Utilisation de graphs pour modéliser le pointage (du plumage) [&,\* = ajout arcs]
    => Système Equation Récurcif + Calcul de point fixe + Très coûteux (n³)
- **[Steensgaard]** Unique flèche de sortie => Noeud plusieurs var
    => Moins Précis + Rapide (presque linéaire) **Mais Pointeur sur Struct = Dégeu**
- Avec Structures et Tableaux => *Ajout Hiérarchie & Abstraction Noeuds*

## Technological Challenges
=> **Envie d'Acheter = Rendre utilisable par les masses**

Targets:
- Software Dev : Rapide, simple, au quotidient
- Software Eng, Système : S'assurer validité globale rapidos
- Eng Qualité : Valider toute l'application, tout les mois (**utilise**)

=> **Atteindre Soft Dev ? Mais Pbs :**
- Code incomplet
- Constructions Spéciales (adresses absolues).
- IDE Immondes, Compilateurs spéciaux ...
- Rendre Résultats compréhensibles (couleurs) :
    - [Vert] : Fiable
    - [Rouge] : Fautes
    - [Gris] : Code mort
    - [Orange] : Non prouvé
    - [Violet] : Violation règle de code
    - [Tool Tip] : Valeures atteignables + détail
(+) Métriques et Détails pour les Eng Qualité

=> **D'autres problèmes sur très gros projets**
- Graph Steensgaard = plat de nouille aux tomates

=> **Outil pour trouver des bugs > Preuves ?**
- (+) Détection que Preuves

## Conclusion
- Pointeur très important
- Multi-tasking présentes de nombreux autres pbs
- Floating Points

=> **N'arrivera jamais à ne pas donner de fausses alarmes (orange)**
- Travailler avec l'utilisateur
