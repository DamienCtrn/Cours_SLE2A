# Model-based Dev for Embedded Control Systems

Conception et Implentation de systèmes de commande embarquée.  
[**> Page Web du Cours**](www-verimag.imag.fr/~tdang/CoursSLE3A.html)

---

## Introduction
#### 1. Which embedded control sys ?
Critical Systems :
- Safety Critical
- Economically Critical

#### 2. Aerospace pioneering role
Control systems => Block diagrams => Formalism => Software => Proofs  
(Automatic generation)

#### 3. State of the art
Steps :
- Model Development
- Simulation & Debugging
- Automatic import
    - Architecture choice
    - Automatic code generation
- Formal verification
- Tests (black box?)

**Safety, Reliability of the implementation ?**
**Real Time ? Determinism ?**

#### 4. Course Content
- Learn Classic methods (Synchronism & 1 Task, Multi-Task)
- Experiment on LEGO Robot

#### 5. Modelisation des systèmes Dynamiques
- Transformée de Laplace (s : continu), en Z (z : discret)
- Définir un Système :
    - Identifier les entrées / sorties
    - Identifier le domaine de temps (continu / discret)
- Diagramme de Bloc = Equation différentielle tranformée (Laplace ou Z)
- Systèmes temps discret : **$X_{n+1} = F(X_n, U_n)$ => Echantillon Précédent**
- Systèmes temps continu : **$X'(t) = F(X(t), U(t))$ => Dérivée / Intégrale**
<!-- $\sum_{i=1}^{10} t_i$ -->
<!-- $\int_0^\infty \mathrm{e}^{-x}\,\mathrm{d}x$ -->
