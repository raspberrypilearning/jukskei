## Cheville

\--- task ---

Sélectionnez le sprite **Peg**. ![Le sprite Peg](images/Peg.png){:width="100px"}

\--- /task ---

### Changer le score

Plus de points si la clé atterrit plus près du piquet.

\--- task ---

```blocks3
+quand je reçois [score v]
+change [Score v] de ((120) - (Atterrissage x))
+change [Lancements gauches v] de (-1)
+définir [Puissance v] sur (0)
```

\--- /task ---

\--- task ---

**Test :** Appuyez sur « t » - vérifiez que le score augmente, que le nombre de lancers diminue de 1 et que la puissance se réinitialise.

\--- /task ---

### Afficher le score

Lorsqu'il n'y a plus de lancers, affichez le score, puis réinitialisez les lancers et le score.

\--- task ---

**Remarque** : Il y a un espace après le mot « Score : » pour séparer le score du mot.

```blocks3
quand je reçois [score v]
changer [Score v] de ((120) - (Atterrissage x))
changer [Lancer à gauche v] de (-1)
définir [Puissance v] à (0)
+si <(Lancer à gauche) = (0)> alors
	dire (joindre [Score: ] (Score)) pendant (2) secondes
	définir [Lancer à gauche v] à (3)
	définir [Score v] à (0)
sinon
```

\--- /task ---

### Dites au joueur de relancer

\--- task ---

```blocks3
quand je reçois [score v]
changer [Score v] par ((120) - (Atterrissage x))
changer [Lancer à gauche v] par (-1)
régler [Puissance v] sur (0)
si <(Lancer à gauche) = (0)> alors
	dire (joindre [Score: ] (Score)) pendant (2) secondes
	régler [Lancer à gauche v] sur (3)
	régler [Score v] sur (0)
sinon
	+dire [Appuyer sur t pour lancer suivant] pendant (1) secondes
+arrêter [ce script v]
```

\--- /task ---

\--- task ---

**Test :** Appuyez à nouveau sur « t ».

- S'il reste des lancers, vérifiez qu'une invite apparaît pour continuer.
- S'il n'y a plus de lancers, vérifiez que le score est affiché, puis les lancers et le score sont réinitialisés.

\--- /task ---
