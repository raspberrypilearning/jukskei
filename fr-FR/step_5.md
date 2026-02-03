## Défi

### Ajoute une célébration !

Ajoute un chapeau de fête et joue une mélodie lorsqu'un score est atteint !

--- task ---

Sélectionne le sprite **Chapeau**. ![Le sprite Chapeau](images/Hat.png){:width="100px"}

--- /task ---

--- task ---

Lorsqu'un score supérieur à (`>`) 200 est atteint, le sprite Chapeau apparaîtra et un son sera joué.

```blocks3
+when I receive [score v]
+forever
	if <(Score) > (200)> then // Essaie de modifier ce score
    	show                              	
    	play sound [Dubstep v] until done 	// Tu peux changer le son
	end
end
```

--- /task ---

--- task ---

Ajoute le code de réinitialisation.

```blocks3
+when [n v] key pressed
+hide
```

--- /task ---

--- task ---

**Test :** appuie sur `N` et joue jusqu'à un score supérieur à 200, puis vérifie que le chapeau s'affiche et que tu entends le son choisi.

--- /task ---

### Afficher les commandes du jeu

--- task ---

Sélectionne la scène et ouvre l'onglet « Arrière-plans ».

--- /task ---

--- task ---

Duplique l'arrière-plan Colline et renomme-le « Commandes ».

--- /task ---

--- task ---

Ajoute du texte à l'arrière-plan des commandes pour indiquer comment contrôler le jeu.

--- /task ---

--- task ---

Ajoute ce bloc de code unique au script « quand la touche n est pressée ».

```blocks3
when [n v] key pressed
stop all sounds
set [Score v] to [0]
set [Puissance v] to [0]
set [Lancers restants v] to [3]
+switch backdrop to [Hill v]
show variable [Puissance v]
show variable [Score v]
show variable [Lancers restants v]
```

--- /task ---

### Choisir un autre sprite Joueur

--- task ---

Choisis le sprite Joueur et sélectionne un nouveau sprite dans la bibliothèque, crée le tien, télécharge une image ou sélectionnes-en un au hasard.

--- /task ---

--- task ---

Assure-toi que ton nouveau sprite possède deux costumes : « lancer » et « immobile » pour conserver l’animation de lancer.

--- /task ---

***

Ce projet a été traduit par des bénévoles:

Jonathan Vannieuwkerke

Michel Arnols

Grâce aux bénévoles, nous pouvons donner aux gens du monde entier la chance d'apprendre dans leur propre langue. Vous pouvez nous aider à atteindre plus de personnes en vous portant volontaire pour la traduction - plus d'informations sur [rpf.io/translate](https://rpf.io/translate).
