# Conférence Michelin

Production de pneu mais pas seulement -> 2k personne en informatique
=> Gestion, Objet Connecté, Data Science, Sécurité

## 1. Introduction aux réseaux LPWA
(Low Power Wide Area) --> IoT : Technologie dans la **table ?!**
- Connectivité sans fil
- Autonomie d'alimentation
- Pérennité des solutions
- Indépendance géographique

**=> Longue Portée & Basse Consommation**

#### 2 Technologies FR :
- *Sigfox* (Déployés dans 36 pays, Grosses levées de fond)
- *LoRaWAN* (Déployés par opérateurs locaux, déployable privé)

#### Architecture :
Noeuds Capteurs > Relay Antenne > Coeur de Réseaux > Backend/Solutions entreprise
=> Communication point à point, faible débit => faible puissance
=> Informations basiques transmises (T°, Pression ...)

#### Points forts :
- *Mode non Connecté* : Economie d'énergie (pas connecté en permanence)
- *Espace Radio Partagé* : Achat de bandes de freq long et compliqué
    (publique = contraint à 1% du temps, faible puissance)

#### 2 Approches différentes :
- *Ultra Narrow Band* [Sigfox] : Bande fine => Plus Puissance
- *Etalement de Spectre* [LoRa] : Message sur plusieurs freq //

#### Comparaison :
| Solution    | Sigfox | LoRaWAN |
|-------------|--------|---------|
| Portée      | +++    | +       |
| Déploiemt   | ++     | -       |
| Scalability | ++     | --      |
| Privé ?     | --     | +++     |


## 2. Produit QuickScan
Mesure de l'usure de pneu + Kilométrage + Identification par Pneu
=> *Prévision changement, Gestion Pneu*

Système - Electronique - Mécanique - Soft Embarqué - Data Science
=> *Equipe Mixte et Pluridisciplinaire*

#### Connectivité :
- **Gateway** : 2G-4G, Abonnement, Achat GSM :(
- **Sigfox** : Connectivité Euro, Agilité, Support, Coût maitrisés :)

#### Alimentation :
- Installation Rapide
- Tenir 3 ans sur un parking (150 000 pneus)
- Minimiser coût de la solution
- Gros appels de courants

=> **Batteries**

## 3. MEMS Evolution 3 :
- Minage (Nicky) WAOW
- Pneu de 4m de diamètre pour les Camions => Risques :
    - Auto-combustion possible
    - Explosion si trop forte pression

=> **Michelin Earthmother Management System**
- Capteurs (Pression, Température, Fixation, Protection)
- Transmission Info (Capteur -> Camion -> Mine -> Michelin)
- Traiter Info (Applications, Rapports)
- Maintenance (Remplacement, Modulabilité ...)
- Support

## 4. Sécurité :
**CERT** : Cyber Sécurité
- IoT => Internet of Vulnerability / DDOS ?
- Aquarium connecté, air conditionné => Vulnérabilités pour Attaques
- Attention aux données postées sur internet (Visibilité, Recherche)
- Exploiter des failles est illégal, les rechercher ne l'est pas
