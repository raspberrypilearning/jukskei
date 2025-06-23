## Défi

### Ajoutez une célébration !

\--- task ---

Sélectionnez le sprite **Chapeau**. ![Le sprite du chapeau](images/Hat.png){:width="100px"}

\--- /task ---

\--- task ---

Montrez le chapeau et jouez un son sur un score élevé.

```blocks3
+quand je reçois [score v]
+pour toujours
	si <(Score) > (200)> alors
    	afficher // Essayer de changer ce score
    	jouer le son [Dubstep v] jusqu'à ce que ce soit fait // Vous pouvez changer le son
	fin
fin
```

\--- /task ---

\--- task ---

Ajouter un code de réinitialisation.

```blocks3
+quand la touche [nv] est enfoncée
+masquer
```

\--- /task ---

\--- task ---

**Test :** Appuyez sur « n » et jouez jusqu'à un score supérieur à 200 - vérifiez que le chapeau s'affiche et que vous entendez le son que vous avez choisi !

\--- /task ---

### Ajouter un écran de contrôle

\--- task ---

Sélectionnez la scène, dupliquez l'arrière-plan de la colline et renommez-le « Contrôles ».

\--- /task ---

\--- task ---

Ajoutez du texte à l’arrière-plan des commandes pour montrer comment contrôler le jeu.

\--- /task ---

\--- task ---

Ajoutez ce bloc de code unique au script « lorsque la touche n est enfoncée ».

```blocks3
lorsque la touche [nv] est enfoncée
arrêter tous les sons
régler [Score v] sur [0]
régler [Power v] sur [0]
régler [Throws left v] sur [3]
+ changer l'arrière-plan sur [Hill v]
afficher la variable [Power v]
afficher la variable [Score v]
afficher la variable [Throws left v]
```

\--- /task ---

### Choisissez un autre sprite de joueur

\--- task ---

Choisissez le sprite du joueur et sélectionnez un nouveau sprite dans la bibliothèque, peignez le vôtre, téléchargez une image ou sélectionnez-en un au hasard.

\--- /task ---

\--- task ---

Assurez-vous que votre nouveau sprite possède deux costumes : « lancer » et « immobile » pour conserver l'animation de lancer.

\--- /task ---
