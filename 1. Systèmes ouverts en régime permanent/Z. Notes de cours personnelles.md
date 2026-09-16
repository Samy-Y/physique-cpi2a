# Rappels et compléments
Un système fermé n'échange pas de matière avec le milieu extérieur. Il peut néanmoins échanger avec lui de l'énergie qu'elle soit sous forme mécanique ou thermique. Le système est défini par une frontière, ce qui permet de le distinguer du milieu extérieur. On peut étendre l'ensemble $\{\text{Système + Extérieur}\}$ à tout l'univers (même si en réalité, seul l'extérieur immédiat du système nous intéresse).

L'énergie totale de l'univers reste constante. Si l'énergie interne du système fermé change, alors celle de l'extérieur a aussi changé. Toute modification de la partie système implique automatiquement qu'il y a eu un échange avec le milieu extérieur. On peut introduire le concept d'énergie totale du système, dont les variations $\Delta E_{tot} = W +Q$ sont postulées par le 1er principe de la thermodynamique. Le terme $E_{tot}$ peut être exprimé comme $E_{tot} = U + E_{c,ma} + E_{p,ma} + ...$ si on prend en compte les énergies d'interaction microscopiques (en petits points dans la formule)  etc..., qui sont en général négligeables (et négligées en pratique). On résume donc $E_{tot}$ à cette expression : $E_{tot} \approx U + E_{c,macro} + E_{p,macro}$.

On introduit aussi la notion d'entropie pour nous permettre de prédire l'évolution d'un système thermodynamique. Un système dans lequel la création d'entropie est impossible est un système qui ne peut pas évoluer et changer. N'importe quelle évolution thermodynamique est accompagnée d'une création d'entropie. L'entropie nous permet aussi de déterminer si une transformation est irréversible.
$$\Delta S = S_{\text{transfert thermique}} + S_{\text{créée}}$$
$$S_{\text{transfert thermique}} = \int \frac{\delta Q}{T_e}$$
Pour n'importe quelle transformation d'un état initial $I$ à un état final $F$, on peut imaginer un chemin *réel* et un chemin *hypothétique* **réversible**. L'entropie créée $S_{prod}$ décide si un chemin est physiquement possible ou non.

---

## Début
On définit le débit massique par $D_m = \frac{\mathrm d m}{\mathrm d t}$.
En introduisant la vitesse d'écoulement $c$, la section $S$ et la masse volumique $\rho$ on trouve que :
$$D_m = \rho S c$$
Un fluide est dit en écoulement permanent si le débit $D_m$ est constant. L'écoulement est laminaire et le régime est permanent.
Si l'écoulement se fait dans un tuyau de forme quelconque selon l'axe $x$, le débit massique peut aussi s'exprimer comme :
$$D_m = \rho(x) S(x) c(x)$$

Un système $\Sigma$ (sans le $dm$ ajouté constamment) en écoulement permanent a une masse, une énergie totale et une entropie constantes.
%% à revoir %%
On peut étudier un système en écoulement permanent de deux manières :
1. **En l'étudiant comme un système fermé $\Sigma \oplus dm$** qui subit une déformation de volume sous $P_1$ d'entrée ou $P_2$ de sortie (et donc $-dV_1 < 0$ ou $dV_2 > 0$).
$$\delta W = \delta W_{pression} +\delta W_{u}$$
$$\delta W_{pression} = \underbrace{\delta W_{pression, entrée}}_{-P_1(-dV_1)} + \underbrace{\delta W_{pression, sortie}}_{-P_2(dV_2)}$$
On introduit le terme de volume massique pour réintroduire $dm$ dans l'expression
$$\delta W_{pression} = (P_1 v_1 - P_2 v_2)\mathrm{d}m$$
Au final, on a $\boxed{\delta W = (P_1 v_1 - P_2 v_2)\mathrm d m + \delta W_u}$
Le terme $\delta W_u$ est dû à l'existence d'une machine externe qui apporte un travail utile.

**Conséquences énergétiques :**
On peut décomposer l'énergie du système $\Sigma \oplus dm$.
$$E_{\Sigma \oplus dm} = E_\Sigma + E_{dm}$$
Et on a $E_{\Sigma \oplus dm}(t + dt) - E_{\Sigma \oplus dm}(t) =\Delta E = \delta W + \delta Q$.
L'énergie interne de $\Sigma$ n'évolue pas en régime permanent. Elle reste donc constante.
$$\implies \Delta E = E_{dm}(t+dt) - E_{dm}(t)$$
Il suffit de faire une analyse énergétique de la masse $dm$ à l'entrée et à la sortie.
À la sortie $(t+dt)$ :
$$E_{dm}(t+dt) = \underbrace{dm u_2}_{\text{énergie interne}} + \underbrace{\frac12 dm c_2^2}_{\text{énergie cinétique}} + \underbrace{gz_2dm}_{\text{énergie pot. pes.}}$$
À l'entrée $(t)$ :
$$E_{dm}(t) = \underbrace{dm u_1}_{\text{énergie interne}} + \underbrace{\frac12 dm c_1^2}_{\text{énergie cinétique}} + \underbrace{gz_1dm}_{\text{énergie pot. pes.}}$$
Finalement, on aboutit à :
$$
\begin{align*}
\Delta E &= dm u_2 + \frac12 dm c_2^2 + gz_2 dm - dm u_1 - \frac12 dm c_1^2 - gz_1 dm \\
&= (P_1 v_1 - P_2 v_2) dm + \delta W_u + \Delta Q \\
\implies \delta W_u + \delta Q &= dm\left[(u_2 + P_2 v_2 + \frac12 c_2^2 + gz_2) - (u_1 + P_1 v_1 + \frac12 c_1^2 + gz_1)\right] \\
&= \boxed{dm\left[(h_2 + \frac12 c_2^2 + gz_2) - (h_1 + \frac12 c_1^2 + gz_1)\right]}
\end{align*}
$$
On retrouve l'expression finale dans la littérature sous le nom de "premier principe de la thermodynamique industrielle" ou \[...]. On peut aussi introduire la notion de travail utile massique en supprimant le terme $dm$ de l'expression, idem pour la notion de transfert thermique massique. En multipliant par $dt$, on retrouve $D_m$ et les énergies deviennent des puissances.

**Bilan énergétique :** Le fluide, quand il est évolution dans une machine industrielle, a la possibilité de voir son bilan être écrit pour une forme infinitésimale du système. On peut donc faire un **bilan élémentaire sur un système élémentaire** (pas microscopique). On obtient :
$$\delta^2W_u + \delta^2 Q = dm(dh + de_c + de_p)$$
($\delta^2$ indique l'élément élémentaire d'ordre 2)
$$\text{ou } dP$$
**Entropie :** En régime permanent, l'entropie totale est constate $dS = 0$.
$$dS = \frac{\delta Q}{T_f} + dm_1s_1 - dm_2s_2 + \delta S_{prod}$$
La masse qui entre apporte avec elle son entropie $dm_1s_1$. La masse sortante emporte $dm_2s_2$ avec elle. Les transferts thermiques contribuent $\frac{\delta Q}{T_f}$ et le terme de production $\delta S_{prod}$ est toujours présent. La variation d'entropie imposée par l'échange de matière est donc réduite à $dm_1s_1 - dm_2s_2$. Comme l'entropie ne varie pas, on trouve alors que :
$$\frac{\delta Q}{T_f} + dm_1s_1 - dm_2s_2 + \delta S_{prod} = 0$$
$$\implies dm(s_2 - s_1) = \frac{\delta Q}{T_f} + \delta S_{prod}$$
%%recoperecoeporoecopeorpeorp%%
$$\implies \delta W_{u,m} \ge \int_{P_1}^{P_2} vdP + (e_{c_2}-e_{c_1}) + (e_{p_2} - e_{p_1})$$
Pour les installations industrielles typiques (qui vont être étudiées), on va systématiquement négliger le terme potentiel $(e_{p_2} - e_{p_1})$, sauf dans les cas où cette cette énergie potentielle a un rôle indispensable (barrages...). Mais on s'intéressera plutôt aux frigos et autres systèmes usuels.
## Applications
### Détente de Joule-Thomson
Il s'agit d'une transformation durant laquelle un fluide passe à travers une paroi poreuse, en vérifiant plusieurs hypothèses :
- l'écoulement du fluide à travers cette paroi est supposé permanent.
- les parois du tuyau sont rigides et adiabatiques
- les pressions et températures sont uniformes de part et d'autre du bouchon poreux
- la conduite est horizontale
- les termes potentiels peuvent être négligés
C'est une détente de gaz isenthalpique. On rappelle que pour un gaz parfait, l'enthalpie $H$ ne dépend que la température $H = f(T)$. Il se peut que le gaz étudié ne soit pas parfait, et que $H = f(T,P)$.
%%voir : turbine, tuyère, compresseur, échange%%

### Compresseur
### Échangeur à co-courants
- Fluide chaud
- Fluide froid
- Les deux fluides sont en écoulement permanent
- Débits constants mais pas forcément de même valeur !
- Il est lieu d'un transfert thermique mais d'aucun travail.
- Variations de $E_c$ et $E_p$ nulles
- **Les échanges avec le milieu extérieur sont impossibles : adiabatique**
- Pour chaque fluide, on peut écrire :
$$\Delta h_i \times \Delta m_i = P_{th_i}$$
- Au final, on aura :
$$\sum_{i} \Delta h_i \times D_{m_i} = 0$$
- *Certains fluides perdent de l'énergie thermique, d'autres en gagnent.*
### Turbine à gaz

