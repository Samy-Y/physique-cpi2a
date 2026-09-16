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

On remarque que $T_1 > T_0$ et $T_2 > T_0$ donc le gaz cède de la chaleur à l'extérieur donc $P_{th} < 0$.

(Énoncé) Les variations d'énergie cinétique étant négligées et les variations d'énergie potentielle étant nulles (turbine horizontale), on a donc $de_c \approx 0$ et $de_p = 0$.

Le premier principe devient donc :
$$D(h_2-h_1) = P_u + P_{th}$$

Le gaz est considéré comme un gaz parfait, donc on peut utiliser la relation $dh = c_p dT$ pour réécrire le premier principe :
$$D c_p (T_2-T_1) = P_u + P_{th}$$

La puissance cédée utile/récupérable est donc :
$$\begin{align*}
P_{cédée} &= -P_u \\
&= D c_p (T_1-T_2) - |P_{th}| \\
&= D c_p (T_1-T_2) + P_{th}
\end{align*}$$

$P_{cédée}$ est maximale quand $P_{th}$ est minimale, c'est-à-dire quand la transformation est adiabatique réversible, donc $\dot\sigma = 0$.

3. **Variation d'entropie entre l'entrée et la sortie :**
$$\Delta s = s_2 - s_1 = \frac{\gamma R}{(\gamma - 1)M}\ln\left(\frac{T_2}{T_1}\right)-\frac{R}M\ln\left(\frac{P_2}{P_1}\right)$$

Après application numérique : $\Delta s = -2 \text{kJ}\cdot\text{K}^{-1}\cdot\text{kg}^{-1}$

L'écoulement est adiabatique, donc $\Delta s = \frac{\dot\sigma}{D} \implies \Delta s \ge 0$.

Il y a donc une contradiction. L'hypothèse d'un écoulement adiabatique est donc fausse. Il y a donc un transfert de chaleur vers l'extérieur.

4. **Puissance cédée à la turbine en la supposant réversible :**

On a $P_{cédée} = D c_p (T_1-T_2) + P_{th}$.

Or la transformation est réversible, donc $\dot\sigma = 0$ et $P_{th} = DT_0\Delta s$.
$$\implies P_{cédée} = D c_p (T_1-T_2) + DT_0\Delta s$$

Application numérique : $P_{cédée} = -600,5 \text{kW}$

5. **Vitesse du fluide à l'entrée et à la sortie et commentaire sur la négligence des variations d'énergie cinétique :**

$$\begin{align*}
\text{On a : } D &= \rho v \Sigma \\
\implies \rho_1 v_1 \Sigma &= \rho_2 v_2 \Sigma \\
\implies v_2 &= \frac{D}{\rho_1 \Sigma} \text{ et } v_1 = \frac{D}{\rho_2 \Sigma}
\end{align*}$$

On a $PV = nRT$ donc :
$$P = \frac{\rho}{M}RT \implies \rho = \frac{PM}{RT}$$
$$\implies v_1 = \frac{D}{\Sigma}\frac{RT_1}{P_1M} \text{ et } v_2 = \frac{D}{\Sigma}\frac{RT_2}{P_2M}$$

Après application numérique, on trouve :
- $v_1 = 0,52 \text{ m/s}$
- $v_2 = 1,72 \text{ m/s}$

On calcule la variation d'énergie cinétique massique :
$$\Delta e_c = \frac{v_2^2-v_1^2}{2} = 1,35 \text{ J/kg}$$

Calculons la puissance cinétique (uniformisation des grandeurs) :
$$P_c = D \Delta e_c = 0,00135 \text{ kW} = 1,35 \text{ W}$$

On a bel et bien $P_c \ll P_{cédée}$ donc la négligence des variations d'énergie cinétique est justifiée.

## Exercice 3

1. **Expression de la température $T_2$ en sortie du compresseur en fonction du taux de compression et de la température d'entrée $T_0$**

On sait que la transformation est adiabatique et réversible. On applique donc les **lois de Laplace** :
$$\begin{align*}
PV^\gamma = \text{cte} &\implies P\cdot \frac{T^\gamma(MR)^\gamma}{P^\gamma} = \text{cte} \\
&\implies T^\gamma P^{1-\gamma} = \text{cte} \\
&\implies P_0^{1-\gamma}T_0^\gamma = P_2^{1-\gamma}T_2^\gamma \\
&\implies T_2 = T_0 \left(\frac{P_2}{P_0}\right)^{\frac{\gamma-1}{\gamma}} = T_0 \beta^{\frac{\gamma-1}{\gamma}}
\end{align*}$$

1. **Expression du travail reçu par le fluide :**

D'après le premier principe, on a :