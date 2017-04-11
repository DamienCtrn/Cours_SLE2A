# Histoire des Bases de données

- **Donnée** : description élémentaire d'une réalité
- **Information** : interprétation de la donnée (mise en contexte, combinaison)
- **Connaissance** : Information avec un sens (logique) -> Vers modélisation

=> ***Base de donnée*** : Ensemble de données organisé
- $Logique$ : organisation
- $Physique$ : mode conservation
- $Vue$
- $Dynamique$

=> 2 Evenements clés : *Relationnel* [1970] & *Web* [1990]

## 1. Préhistoire
[1950] **Bandes magnétiques**
- Fichiers séquentiels
- Traitement simple (tri, fusion, recherche)

[1960] **Disques Magnétiques**
- Accès Direct
- Avancées : Indexation, accélération de l'accès

## 2. Premiers Modèles
- [1966] Premier SGBD d'IBM en (IMS) **Modèle hiérarchique** -> $XML$   
*organisation simple mais peu adaptable*

- [1962] Premier SGBD de l'histoire (IDS) **Modèle Réseau**  
*organisation plus souple MAIS pas d'indépendance des données*

### a. Le Schéma conceptuel
- [1976] **Schéma entité-association** pour aider à l'organisation
- [1995] **UML** fusion de plusieurs travaux

### b. Le Modèle Relationnel
Développé par IBM en 1970 avec plusieurs avantages :
- Base mathématique : algèbre relationnelle
- Indépendance des données

Mais **efficacité** ?  
=> Difficile ... (*explosion combinatoire*)  
=> Recherche pas optimal mais **raisonnable** (temps exécution)

#### <> [1974] System-R
- **Invention SQL** et sa compilation
- Optimisation des requètes

#### <> [1973] Ingres
*Interactive Graphical and Retrieval System*
- Utilisation Unix et QUEL
- Utilise SGF d'Unix

Puis premiers produits commerciaux :
- [1979] **Oracle**
- [1983] **IBM DB2**

### c. Bases de données à objets
- Utilisation de la persistance des données (sauvegarde des variables)
- Accès rapide par pointeurs

## 3. Transactions
- Propriétés ACID (Gray 1981)
- Journalisation (enregistrement de chaque opération)
- Validation à 2 phase (pour faire atomicité)
