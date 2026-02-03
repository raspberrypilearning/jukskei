## Uitdaging

### Voeg een viering toe!

Voeg een feestmuts toe en speel een deuntje als een score is bereikt!

--- task ---

Selecteer de **Hoed**-sprite. ![De Hoed-sprite](images/Hat.png){:width="100px"}

--- /task ---

--- task ---

Als een score hoger dan (`>`) 200 wordt bereikt, verschijnt de Hoed-sprite en wordt er een geluid afgespeeld.

```blocks3
+when I receive [score v]
+forever
	if <(Score) > (200)> then // Probeer deze score te veranderen
    	show                              	
    	play sound [Dubstep v] until done 	// Je kunt het geluid veranderen
	end
end
```

--- /task ---

--- task ---

Voeg resetcode toe.

```blocks3
+when [n v] key pressed
+hide
```

--- /task ---

--- task ---

**Test:** Druk op `N` en speel tot een score boven de 200. Controleer vervolgens of het hoedje verschijnt en of je het gekozen geluid hoort.

--- /task ---

### Toon de spelbesturing

--- task ---

Selecteer het speelveld en open het tabblad Achtergronden.

--- /task ---

--- task ---

Dupliceer de achtergrond 'Hill' en hernoem deze naar 'Besturing'.

--- /task ---

--- task ---

Voeg tekst toe aan de Besturings-achtergrond om te laten zien hoe je het spel bestuurt.

--- /task ---

--- task ---

Voeg dit ene codeblok toe aan het script 'wanneer toets n wordt ingedrukt'.

```blocks3
when [n v] key pressed
stop all sounds
set [Score v] to [0]
set [Kracht v] to [0]
set [Aantal resterende worpen v] to [3]
+switch backdrop to [Hill v]
show variable [Kracht v]
show variable [Score v]
show variable [Aantal resterende worpen v]
```

--- /task ---

### Kies een andere Speler-sprite

--- task ---

Kies de Speler-sprite en selecteer een nieuwe sprite uit de bibliotheek, ontwerp er zelf een, upload een afbeelding of selecteer een willekeurige sprite.

--- /task ---

--- task ---

Zorg ervoor dat je nieuwe sprite twee uiterlijken heeft: 'worp' en 'stilstaan', zodat de worp-animatie behouden blijft.

--- /task ---

***

Dit project werd vertaald door vrijwilligers:

Iny van Beuningen

Robert-Jan Kempenaar

Dankzij vrijwilligers kunnen we mensen over de hele wereld de kans geven om in hun eigen taal te leren. Jij kunt ons helpen meer mensen te bereiken door vrijwillig te starten met vertalen - meer informatie op [rpf.io/translate](https://rpf.io/translate).
