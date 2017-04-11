# Histoire de l'Internet
- [1970] ARPANET
- ...
- [1995] Diffusion du Web

## Le Role de l'ARPA
$Advanced Research Projects Agency$ : Initialement sur le spacial jusqu'à création de la *NASA*.  
=> **Informatique**

$Idées$ : Connecter les ordinaters via une interface uniforme => **ARPANET**.

- *Communication par packet* : redondance, survivant aux attaques, fragmentation en blocs
- *Architecture à 2 Niveaux* : différenciation entre Hôtes et nœuds du réseau (IMP), interfaces, facilement extensible
- *Protocole hôte-hôte* : socket envoi/réception, processus => **NCP**

$Début$ :

- [Octobre  1969] : Premier échange
- [Décembre 1969] : 4 Hôtes connectés  

*puis croissance rapide ...*

## En France : Cyclades
- [1971] Début du Projet
- [1973] 3 sites dont 1 à l'IMAG
- [1978] Arrêt du profit de Transpac

Arrêt due à la forte opposition de la DGT (*Direction Générale des Télécommunication*)  
=> **Projet Transpac** => **Minitel** (peu avancé sur le plan technique)

Mais Innovations de Cyclades reprises par ARPANET :
- **Le datagramme** ~-> TCP
- **Le contrôle de flux** : Fenêtre Glissante

## De NCP à TCP/IP
$Idée$ : Réunir plusieurs réseaux

- [1972] Ne pas toucher aux réseaux existants et restant indépendants,  
    Pas de garantie, Connecté par des boîtes noires {routeurs} (sans état)
- [1973] **TCP : Transmission Control Protocol**
- [1974] Maximum de 256 Réseaux ...

TCP très bon pour accès distants et transferts de fichiers mais pas pour la voix
(*Perte de packets problématiques pour certaines applications*)

**=> IP, UDP & TCP**  
**=> Protocoles en Couches**

## Adresses IP ...
Différenciation en 3 classes : Nb Réseaux + Nb Hôtes = 31 bits ?  
**=> Problèmes :**
- Débordement de la classe C
- Espace des noms & annuaire
- Limites de l'espace des Adresses
- Saturation des ressources

**=> Solutions :**
- Organisation en Domaines
- [1983-84] Service d'annuaire réparti : **DNS : Domain Name System**  
    *Caches, Hiérarchie des serveurs de noms ...*
- IPv6 (128 bits)
- CIDR (*Classless InterDomain Routing*) utilisant des masques : nouvelle partition.
- NAT (*Network Address Translation*) Hôtes d'un réseau (routeur) gère les IPs
- Contrôle de la fenêtre pour controler la congestion dans TCP

## De l'ARPANET à l'Internet
- [1983] NCP => TCP/IP
- [1984] DNS
- [1990] Arrêt ARPANET
- [1995] Prise en charge de la dorsale par entreprises privées

## Recherche de l'information ... avant le Web (fin 1980s)
- $Archie$ : Premier moteur de recherche
- $WAIS$ (*Wide Area Information Server*) : avec index
- $Gopher$ : Protocole de recherche de documents

## Défis
- **Sécurité**
- **Aspect Societaux**
- **Transition vers IPv6**
- **Mobilité** : Accès mobile
