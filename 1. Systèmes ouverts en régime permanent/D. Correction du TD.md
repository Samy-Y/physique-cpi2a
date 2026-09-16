## Rappel de ce qu'est la "thermodynamique"

La thermodynamique concerne l'étude des échanges thermiques/énergétiques entre un système et le milieu extérieur aka. l'univers.

Les systèmes thermodynamiques ouverts concernent ceux qui échangent de la matière (généralement un fluide) avec le milieu extérieur.

La thermodynamique est basée sur plusieurs principes :

- **Le 1er principe de (...) :**
	- Le premier principe stipule que l'énergie totale d'un système isolé est constante. Il peut s'écrire sous la forme :
	$$dE = \delta W + \delta Q$$
	- Le premier principe est un principe de *conservation*. Il est insuffisant pour étudier les systèmes thermodynamiques de matière globale.
- **Le 2e principe de (...) :**
	- Le deuxième principe stipule que l'entropie d'un système isolé ne peut qu'augmenter ou rester constante.
	$$dS = \delta S_{éch}+ \delta S_{cré} \geq 0$$
	- Pour un système isolé, le terme $\delta S_{éch}$ est nul, donc $dS = \delta S_{cré} \geq 0$.
	- Le deuxième principe est un principe d'*évolution*. Il permet de déterminer le sens d'évolution d'un système lors d'une transformation.
Une grandeur conservative reste constante pour un système isolé.
- L'énergie totale est une grandeur conservative.
- L'énergie interne et l'entropie n'en sont pas.
- La masse est une grandeur conservative.

>[!NOTE] Système isolé
> Quand on parle de "système isolé", on parle de système sans échange thermique, mécanique ou de matière avec le milieu extérieur.

Un grandeur extensive/additive est additionnée lors de l'union de deux systèmes pour former un nouveau système global.
$$\Sigma = A \cup B \implies X_\Sigma = X_A + X_B$$

Pour utiliser le premier et second principe pour l'étude d'un système ouvert, il faut définir un nouveau système $\Sigma^*$ qui est défini à deux instants $t$ et $t+dt$ pour contenir la masse entrante $dm_e$ et la masse sortante $dm_s$ (qui seront généralement égales pour un système en régime permanent).

Le système $\Sigma^*$ est donc un système fermé, et on peut appliquer les principes de la thermodynamique à ce système.

---

## Exercice 1
*Questions de cours - Ignoré*

## Exercice 2
1. **Rappel du premier principe pour un fluide en écoulement stationnaire :**
   $$\begin{align*}
   d(H+E_c+E_p) &= \delta W + \delta Q \\
   \implies (dh+de_c+de_p) &= \delta w + \delta q \\
   \implies D \times (dh+de_c+de_p) &= D \times (\delta w + \delta q) \\
   \implies D(dh+de_c+de_p) &= \frac{dm}{dt}\delta w_u + \frac{dm}{dt}\delta q \\
   \implies (dh+de_c+de_p)D &= P_u + P_{th}
   \end{align*}$$
**Rappel de l'expression du deuxième principe pour un fluide en écoulement stationnaire :**
$$\begin{align*}
dm\cdot ds &= \delta S_{éch} + \delta S_{cré} \\
\implies dm\cdot ds &= \frac{\delta Q}{T_0} + \delta S_{cré} \\
\text{Or on sait que : } \delta Q &= P_{th} dt \\
\implies dm\cdot ds &= \frac{P_{th} dt}{T_0} + \delta S_{cré} \\
\implies \frac{dm}{dt} ds &= \frac{P_{th}}{T_0} + \frac{\delta S_{cré}}{dt} \\
\implies D(s_2-s_1) &= \frac{P_th}{T_0} + \dot\sigma
\end{align*}$$

$\dot\sigma$ représente le taux de création d'entropie, soit $\frac{dS_{cré}}{dt}$, aussi noté $\sigma^{cre}$.

2. **Commentaires sur les échanges entre le gaz et l'extérieur :**

On remarque que $T_1 > T_0$ et $T_2 > T_0$ donc le gaz cède de la chaleur à l'extérieur.

(Énoncé) Les variations d'énergie cinétique étant négligées et les variations d'énergie potentielle étant nulles (turbine horizontale), on a donc $de_c \approx 0$ et $de_p = 0$.

Le premier principe devient donc :
$$D(h_2-h_1) = P_u + P_{th}$$

D'après le deuxième principe, on a :
$$\dot\sigma \ge 0$$
Ce qui implique que :
$$D(s_2-s_1) \ge \frac{P_{th}}{T_0}$$