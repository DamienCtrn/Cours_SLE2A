# Model-based Dev for Embedded Control Systems

## Stabilité des systèmes
- Oscillation ? Reconverge vers un pt d'équilibre ?
- Utilisation Feedback
=> Dénominateur != 0
=> Racines à partie réelles négatives !

Méthode de Lyapunov pour prouver Stabilité

## Simulink
- Library :
    - Temps continu
    - Temps discret
    - Displays

## Echantillonnage
--> Construction d'un controleur continu et l'échantillonner
(*Echantillonner = Approcher le continu*)

#### Shéma d'Euler
**$x(t+T) \approx x(t) + T*x'(t)$**

Approximations :

| Nom              | $z \approx$                 | $s \approx$                         | Stab |
| ---------------- | --------------------------- | ----------------------------------- | ---- |
| Euler en avant   | $1 + sT$                    | $\frac{z - 1}{T}$                   | Nope |
| Euler en Arrière | $\frac{1}{1 - sT}$          | $\frac{z - 1}{zT}$                  | Yep  |
| Trapézoidal      | $\frac{1 + sT/2}{1 - sT/2}$ | $\frac{2}{T} * \frac{z - 1}{z + 1}$ | Yep  |


#### Shanon-Nyquist
$2*f_{max~sys} < f_{ech}$
