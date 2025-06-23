## Joueur

\--- task ---

Ouvrez le [projet de démarrage](https://scratch.mit.edu/projects/1187059894/editor/){:target="_blank"}.

\--- /task ---

Le projet de démarrage contient du code de démarrage et tous les sprites dont vous avez besoin.

\--- task ---

Sélectionnez le sprite **Joueur**. ![The Player sprite](images/Player.png){:width="100px"}

\--- /task ---

### Lancer!

Animez le joueur lorsqu'il lance une clé.

\--- task ---

Dans le bloc « quand je reçois » {:class="block3events"}, changez de costume.

```blocks3
+when I receive [throw v]
+switch costume to [throw v]
+wait (1) seconds
+switch costume to [still v]
```

\--- /task ---

\--- task ---

**Test:**

- Appuyez sur « n » pour démarrer une nouvelle partie, puis sur « t » pour démarrer un nouveau lancer - vérifiez que la barre d'alimentation passe de 0 à 100.

- Appuyez sur « espace » pour arrêter la barre de puissance - vérifiez que le joueur change de costume pour le costume de lancer, puis revient au costume fixe

\--- /task ---
