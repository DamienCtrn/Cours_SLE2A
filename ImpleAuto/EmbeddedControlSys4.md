# Model-based Dev for Embedded Control Systems

## Monotâche
- Conçoit avec parallèlisme de description
- Mais compilé en ordonnancement statique
- Mais ordonnancement doit être possible !
  **WCET (Worst Case Execution Time)** < périodicité
  => Découpage de tâches mais difficile à faire

## Multitâches
- Synchrone = horloge commune à tout le monde
- Communications déterministes :
	- pas de boucles combinatoires (sortie sur entrée sans buffer)
	- si pas de retard, il faut au moins un buffer

- Ordonnancement Dynamique : **Préemption, Priorités**
- Minimum de RTOS ici: priorités statiques ...
- Communications non bloquantes, par mémoires partagée
  (cohérence assurée avec prio et buffers)

*Exemple* :
- 1 tâche urgente rapide et 1 tâche fond longue
- horloges périodiques harmoniques
- U prioritaire sur F
- Communications F vers U via retard logique
- Communications U vers F libres
- Contraintes WCET satisfaites
- Donc implémentation :
	- multitâche préemptive et fidèle à simu
	- déterministe et sans blocage
