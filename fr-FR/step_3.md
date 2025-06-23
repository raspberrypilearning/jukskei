## Skey

\--- task ---

Sélectionnez le sprite **Skey**. ![Le sprite Skey](images/Skey.png){:width="100px"}

\--- /task ---

### Déplacez-vous vers la cheville

Définissez la position initiale de la touche.

\--- task ---

```blocks3
+quand je reçois [lancer v]
+aller à x : (-127) y : (29)
+définir le style de rotation [tout autour de v]
+pointer vers (Stylo v)
+démarrer le son (Sirène sifflet v)
```

\--- /task ---

Lancez l'arc dans les airs

\--- task ---

```blocks3
quand je reçois [lancer v]
aller à x : (-127) y : (29)
définir le style de rotation [tout autour de v]
pointer vers (Stylo v)
démarrer le son (Sifflet de sirène v)
+répéter jusqu'à <(distance à (Stylo v)) < (Atterrissage x)>
  tourner dans le sens des aiguilles d'une montre (15) degrés
  se déplacer (10) pas
  pointer vers (Stylo v)
fin
+démarrer le son (Sifflet cognant v)
+attendre (0,5) seconde
```

\--- /task ---

\--- task ---

**Test :** Appuyez sur « t » pour vérifier que la touche se déplace dans l'air en arc de cercle et que les sons de lancer et d'atterrissage sont émis.

\--- /task ---

### Réinitialiser

Réinitialisez la position de la clé après son atterrissage.

\--- task ---

```blocks3
quand je reçois [lancer v]
aller à x : (-127) y : (29)
définir le style de rotation [tout autour de v]
pointer vers (Stylo v)
démarrer le son (Sifflet de sirène v)
répéter jusqu'à <(distance à (Stylo v)) < (Atterrissage x)>
  tourner dans le sens des aiguilles d'une montre (15) degrés
  déplacer (10) pas
  pointer vers (Stylo v)
fin
démarrer le son (Sifflet coupant v)
attendre (0,5) seconde
+aller à x : (-136) y : -11
+pointer dans la direction (120)
```

\--- /task ---

### Notation des déclencheurs

\--- task ---

```blocks3
quand je reçois [lancer v]
aller à x : (-127) y : (29)
définir le style de rotation [tout autour de v]
pointer vers (Stylo v)
démarrer le son (Sifflet de sirène v)
répéter jusqu'à <(distance à (Stylo v)) < (Atterrissage x)>
  tourner dans le sens des aiguilles d'une montre (15) degrés
  déplacer (10) pas
  pointer vers (Stylo v)
fin
démarrer le son (Sifflet coupant v)
attendre (0,5) seconde
aller à x : (-136) y : -11
pointer dans la direction (120)
+diffusion (score v)
```

\--- /task ---