# ELSYS Design
Appartient Advans Group comme Avisto (Android), Mecagine et TES

-> Dev Sys Embarqué Contraint sous RTOS
- Presentation
- Sys temps réel
- Mise en oeuvre
- Cloisonnement

### Intervenant
Benoit Magnier : Ingénierie des sys électroniques, RTOS Custom, Drivers

### Entreprise
- Micro elec
- Logiciel Applicatif
- Services 65%
- Innovation avec 4 starts-up Grenobloises
- Aérospatiale, Défense, Energie, Médical, Multimédia, Télécoms, Transport, Semiconducteurs ...
- Ingénierie avant tout

## 1. Systèmes Temps réels
**Notions** :
- Abstraction Machine Physique
- Interface simple à l'utilisateur
- Gestion Ressources, Ordonnancement

=> **Multi-tâches** :
- Concurrence (time sharing ...)
- Préemption (suspension ...)
- Réentrance (sections critiques, exclusion mutuelles, Synchro, Héritage Prio, Dead Lock)

=> **Temps Réel** :
- Déterminisme sur le temps et l'ordre de traitement
- Vitesse traitement dépend besoin (Navigation, Pilotage ...)
- *Exemples :*
    - Pilotage Antenne 4 axes, Linux-RT, Régulation 20ms
    - Données Position Avion, Affichage tableau bord
- Section critiques à minimiser
- Optimisation à éviter sur certaines sections : *volatile*

=> **Problème Temps Réel ?** :
- **BUG** : Chercher à reproduire le problème, stresser le système plutôt que de l'éviter
- Sans RTOS : Boucle Scrutation > Perte Events
- Avec RTOS : Sequencement préemptif > Getion Ressources, temps reponse garantit, Interruptions
  Choix dépend Application : (Fonctionnalités, Perfs, Encombrement, Offre Logiciel, Communications, Outil de Dev (debugger, simulateur), Coût, Latence interruptions ...

=> **RTOS ?** :
- Logiciel écrit en C/Assembleur adapté à CPU cible
- BSP : Drivers pour un carte donnée
- API : Librairie de fonctions

## 2. Mise en oeuvre
*Idéal* : Dev cycle en V
*Réaliste* : Hypothèses pas forcément validées, Changement exigences, Problème Technique (Archi, HW, Bug)

=> **Solutions** :
- Etudes, Dérisquage, Analyse risques, Actions préventives
- Identifier différentes fonctions : priorités, Identifier contraintes temps-réel : pire cas, Sureté de Fonctionnement ...
- *Exemples* :
    - **Système dépollution fumées** : OS préemptif uCOS-II, Automate, Détection Erreures, Tests, Problème section critique pendant la phase de pilotage : Arc Électrique

=> **Etapes Dev** :
- Preuves de concept sur carte d'évaluation (test archi choisie, pilotage)
- Test sur table (Intégration hard / soft)
- Test sur boitier final (connecteurs façade ?! -> Difficile)

## 3. Notions de Cloisonnement (OS)
*Exemple* point de vente : **IHM**[peut planter -> OS], **module paiement**[doit jamais planter -> Bare Metal]
=> Rassembler tout ?
- Cloisonnement Logiciel et non matériel
- Réduction coûts
- Virtualisation -> CPU virtuel : **HYPERVISEUR**
    - Partage de ressources avec machines virtuelles

=> **Cloisonnement ?** :
- *Mémoire* : Chaque process confiné à sa zone mem (grâce MMU)
- *Temps* : Découpage en timeslices : on sait exactement qui peut s'exécuter
- *Exemples* :
    - QNX Neutrino 6.6 : Partitionnement adaptatif Temps
    - Wind River VxWorks 7 : Protec Mem + Partitionnement Temps
    - Green Hils software integrity 11.04
- *C'est notre projet !* : Boitier qui communique sur 2 réseaux
- Aucun Risque Corruption, Pas mem partagée, Pas com entre cloisons
    - Communications alors ? :o
    - API de com fournie **a utiliser correctement** : GHS INTEGRITY
        - **VAS : Virtual Address Space** :
            - *Mécanismes* Region Mémoire, Connection, Semaphore, Vérif intégrité des données, Timeout (blocage ressources, non réponse requète ...)
- *C'est notre projet ! 2* : Ressource Manager, Clients, Server
    => Sécurisation par protocoles statiques (Handshake)

=> **Scheduling ?** :
- Priorité inter-tâches
- Cadencement / Protection par Sémaphores, Mutex
- Ordonnancement standard ou Par partition temporelle courante (Budget) ou Estimation et allocation dynamique du partitionnement
