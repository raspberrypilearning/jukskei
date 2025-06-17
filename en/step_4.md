## Peg

--- task ---

Select the **Peg** sprite. ![The Peg sprite](images/Peg.png){ width: 200px; }

--- /task ---

### Change the score

More points if the skey lands closer to the peg.

--- task ---

```blocks3
+when I receive [score v]
+change [Score v] by ((120) - (Landing x))
+change [Throws left v] by (-1)
+set [Power v] to (0)
```

--- /task ---

--- task ---

**Test:** Press `t` - check the score increases, the number of throws reduces by 1 and the power resets.

--- /task ---

### Display the score

When there are no throws left, show the score, then reset the throws and score.

--- task ---

**Notice**: There is a space after the word 'Score: ' to separate the score from the word.

```blocks3
when I receive [score v]
change [Score v] by ((120) - (Landing x))
change [Throws left v] by (-1)
set [Power v] to (0)
+if <(Throws left) = (0)> then
	say (join [Score: ] (Score)) for (2) seconds
	set [Throws left v] to (3)
	set [Score v] to (0)
else
```

--- /task ---

### Tell the player to throw again

--- task ---

```blocks3
when I receive [score v]
change [Score v] by ((120) - (Landing x))
change [Throws left v] by (-1)
set [Power v] to (0)
if <(Throws left) = (0)> then
	say (join [Score: ] (Score)) for (2) seconds
	set [Throws left v] to (3)
	set [Score v] to (0)
else
	+say [Press t for next throw] for (1) seconds
+stop [this script v]
```

--- /task ---

--- task ---

**Test:** Press `t` again. 

- If there are throws left - check a prompt appears to continue.
- If there are no throws left - check the score is shown and then the throws and score are reset.

--- /task ---
