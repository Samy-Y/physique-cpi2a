## Définitions
- **Système ouvert :** Système qui échange de la matière avec le milieu extérieur.
	- On considère généralement un système $\Sigma$ constitué d'un *volume de contrôle* fixe dans l'espace à travers lequel entre et sort le fluide.
	- Ce système peut échanger avec le milieu extérieur (transferts thermiques, mécaniques et de fluide).
- **Écoulement :** Transfert macroscopique de matière.
- **Écoulement permanent :** La masse qui entre dans le volume de contrôle par unité de temps est égale à la masse qui en sorte par unité de temps (*conséquence*)*.
	- La masse située dans le volume de contrôle est constante.
	- Les grandeurs additives associées au volume de contrôle (énergie...) sont constantes dans le temps.
	- Le débit massique est défini par : $D_m = \frac{dm}{dt}$. $dm$ est la masse qui traverse une section $S$ du système pendant $dt$.
## Bilan énergétique
Les bilans énergétiques dans un système ouvert à écoulement permanent entre $t$ et $t+dt$ sont calculables en considérant le système fermé $\Sigma \cup dm$ (le volume de contrôle et la masse $dm$).

En écoulement permanent, le système $\Sigma$ considéré a une masse $m$, une énergie totale $U$ et une entropie toutes constantes (**ADMIS**). *L'état macroscopique du système ne dépend plus du temps.*
### Application du 1er principe en système ouvert (régime permanent)
On définit un système fermé déformable $S$ à deux instants voisins :
- À l'instant $t$ : $S(t) = \Sigma \cup \mathrm{d}m_e$
- À l'instant $t+\mathrm{d}t$ : $S(t+\mathrm{d}t) = \Sigma \cup \mathrm{d}m_s$
Régime permanent $\implies \mathrm{d}m_e = \mathrm{d}m_s = \mathrm{d}m$.
#### Échanges avec l'extérieur pendant $\mathrm{d}t$
- **Transfert thermique reçu :** $\delta Q = q \cdot \mathrm{d}m$ (à travers les parois de $\Sigma$).
- **Travail utile reçu :** $\delta W_u = w_u \cdot \mathrm{d}m$ (arbres mobiles, turbines, compresseurs).
- **Travail des forces de pression (forces de transvasement) :**
	- En entrée (moteur) : $\delta W_{p,e} = + p_e \mathrm{d}V_e = + \frac{p_e}{\rho_e}\mathrm{d}m$
	- En sortie (résistant) : $\delta W_{p,s} = - p_s \mathrm{d}V_s = - \frac{p_s}{\rho_s}\mathrm{d}m$
	- Soit : $\delta W_p = \left(\frac{p_e}{\rho_e} - \frac{p_s}{\rho_s}\right)\mathrm{d}m$
#### Premier principe pour $S$ entre $t$ et $t+\mathrm{d}t$
$$\mathrm{d}(E_c + E_p + U)_S = \delta W_u + \delta W_p + \delta Q$$
Comme l'état macroscopique de $\Sigma$ est stationnaire, $E_{\Sigma}(t+\mathrm{d}t) = E_{\Sigma}(t)$ :
$$\mathrm{d}E_S = \mathrm{d}m \left[ (u_s - u_e) + \Delta e_c + \Delta e_p \right]$$
En regroupant le travail de pression avec l'énergie interne ($h = u + p/\rho$) :
$$\Delta h + \Delta e_c + \Delta e_p = w_u + q$$
On peut exprimer le reste des variations d'énergie par :
$$\begin{cases}
dU = U_S(t+dt) - U_S(t) = (u_s-u_e)dm\\
dE_c = (e_{c,s}-e_{c,e})\cdot dm\\
dE_p = (e_{p,s}-e_{p,e})\cdot dm
\end{cases}$$
On peut donc réécrire le premier principe comme (après avoir simplifié par $dm$) :
$$(e_{c,s}-e_{c,e}) + (e_{p,s}-e_{p,e}) + (u_s-u_e) = \left(\frac{p_e}{\rho_e}-\frac{p_s}{\rho_s}\right)+w_u + q$$
En introduisant le terme d'enthalpie massique du fluide :
$$h = u + \frac{P}{\rho}$$
qu'on peut facilement obtenir à partir de $H = U + PV$ via $V = \frac{dm}{\rho}$ puis en divisant par $dm$...
On trouve l'expression suivante :
$$(e_{c,s}-e_{c,e})+(e_{p,s}-e_{p,e})+(h_s-h_e) = w_u+q$$
On peut aussi définir les puissances mécaniques utiles et thermiques :
$$\begin{cases}
w_u \cdot D_m = w_u \cdot \frac{dm}{dt} = \frac{W_u}{dt} = P_u\\
q \cdot D_m = \dots = P_q
\end{cases}$$
Pour trouver :
$$P_u + P_q = D_m\left[e_{c,s}-e_{c,e}) + (e_{p,s}-e_{p,e}) + (h_s-h_e)\right]$$
(les termes relatifs au travail de pression ont été absorbés par l'enthalpie)
On peut aussi réécrire l'expression différentielle (sans puissances) pour trouver :
$$de_c + de_p + dh = \delta w_u + \delta q$$
L'énergie cinétique massique et l'énergie potentielle massique sont données par :
$$\begin{cases}
e_c = \frac12 c^2\\
e_p = gz
\end{cases}$$
Et on obtient l'expression du premier principe dit "industriel" :
$$\Delta(h+\frac12 c^2 + gz) = w_u + q$$

### Application du 2nd principe en système ouvert
$$\Delta s = s_{\text{échangée}} + s_{\text{créée}}$$
avec $s_{\text{échangée}} = \frac{q}{T_{ext}}$ l'entropie massique échangée et $s_{\text{créée}} \ge 0$ l'entropie massique créée. $T_{ext}$ est la température de la surface à travers laquelle se font les échanges thermiques. En appliquant l'identité thermodynamique suivante :
$$dh = Tds + vdp = Tds + \frac{dP}{\rho}$$
En remplaçant dans l'équation du bilan industriel $q = T\cdot s_{\text{échangée}}$ on trouve :
$$w_u = \Delta\left(\frac12 c^2\right) + \Delta(gz) + \int_e^s \frac{dP}{\rho} + s_{\text{créée}}$$
Comme $s_\text{créée} \ge 0$, alors $w_u \ge \Delta\left(\frac12 c^2\right) + \Delta(gz) + \int_e^s \frac{dP}{\rho}$


