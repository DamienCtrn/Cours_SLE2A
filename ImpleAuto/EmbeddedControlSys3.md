# Model-based Dev for Embedded Control Systems

## Controle de commande sûr
- Matériel
- Logiciel de base (Firmware)
- Logiciel Applicatif

=> **Problèmes**:
- Fonctionnalité (calculer juste)
- Temps réel (calculer vite)

=> **Conception** :
- **BAD car non-bornés** : Alloc Dynamique, Récurcivité, While, Concurrence, Communication bloquante

## Conception -> Implémentation Monotâche
Conception simple avec Machine à Mémoire (sorte de FSM)  
Fonction appelée à chaque événement ou périodiquement
=> ***BARE METAL*** (sans OS, fonctionnalité bien définie)

Au final,
- Gros système = plusieurs petits systèmes avec concurrence et parallèle
- Block Diagrams = Spec
- Multitâches = (+) de Problèmes (Perf, Blocages, Priorité)

Passage d'un Diagramme Complexe vers Monotâche ? => **Compilation** (Scale, Simulink)

## Le TP LEGO ?
**Model Based Design** :
- Conception conjointe procédé/processus
- Outil Ref pour automaticien (Simulink)
- Génération Automatique du code avec Scade et Lustre
    - Traducteur *mdl2lus* [Simulink > Lustre] : filtre pour rejetter les modèles douteux
    - Traducteur *lus2c* [Lustre > C] ??
- Utilisation Plateforme NXT-OSEK pour prog en C
- Tâches Périodiques :
    - Positionnement des entrées
    - Appel du Step
    - Raffraichissement du LCD
    - Finalisation de la tâche

## Chaine de Compilation
[.mdl] > [ .lus] > [.c & .h] | [kernel_cfg, makefile] > [.bin]
ajouter dans .bashrc :
``` bash
source /user/5/raymonddp/mdl2lus2osek/SETENV.sh
```
exemple dans :
``` bash
mdl2lus2osek/current/
```
## Modèle
- Programme dans un seul fichier
- Simu : Fixed-step / discrete
- Types de données renseignés (bool, int ...)
