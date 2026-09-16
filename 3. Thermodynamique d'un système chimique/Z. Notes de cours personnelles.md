- Définition d'un système chimique
- Définition d'une réaction chimique
- Écriture de "*de Donder*" pour les réactions chimiques :
	- Constituants $A_i$
	- Coefficients stœchiométriques $\nu_i$
		- $\nu_i < 0$ pour les réactifs
		- $\nu_i > 0$ pour les produits
	- Symbolisée : $\sum_{i=1}^N \nu_i A_i = 0$
- Bilan de coefficients stœchiométriques d'une réaction : $\Delta \nu = \sum_i \nu_i$
	- Pour ${N_2}_{(g)}+3{H_2}_{(g)} \leftrightarrow 2{NH_3}_{(g)}$ on trouve $\Delta \nu = -2 < 0$
	- Représente les moles disparus de la réaction (variations internes &c &c)
		- Pas de perte de matière ; PERTE DE MOLES
## Caractérisation de l'état thermodynamique d'un système chimique
- Les paramètres d'état d'un système thermodynamique est *techniquement* défini par $(T,P,n_i)$ avec $n_i$ le nombre de moles de $A_i$. C'est $N+2$ paramètres d'état.
- On réduit le nombre de paramètres d'état à 3 en compressant les $n_i$ au terme $\xi$ qui correspond à l'avancement d'une réaction chimique, défini par $d\xi = \frac{dn_i}{\nu_i}$.
%% refaire démonstration %%
## Bilan énergétique : Chaleurs de réaction
- On s'intéresse aux chaleurs de réaction au cours de transformations monothermes et isobares.
- Enthalpie molaire de réaction : $\Delta_r H(T,P,\xi) = \left(\frac{\partial H}{\partial\xi}\right)_{P,T}$
- La variation d'enthalpie entre deux états d'avancement $\xi_i$ et $\xi_f$ à $T$ et $P$ constants est :
$$\Delta H = \int_{\xi_i}^{\xi_f} \Delta_r H\,d\xi$$
- $\Delta H$ s'exprime en $J$.
- $dh = \delta Q$ donc $\Delta H = Q_p$ la chaleur de réaction isobare
- 