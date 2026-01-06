## Scoring on the peg

--- task ---

Select the **peg** sprite. ![The Peg sprite](images/Peg.png){:width="100px"}

--- /task ---

### Change the score

The skey receives more points if it lands closer to the peg.

--- task ---

```blocks3
+when I receive [score v] // Receive the broadcast message from before. 
+change [Throws left v] by (-1)
+change [Score v] by ((120) - (Landing x))
+set [Power v] to (0)
```

--- /task ---

--- task ---

**Test:** Press `T'. Check the score increases and that the number of throws reduces by 1 and the power resets.

--- /task ---

### Display the score

When there are no throws left, show the score, then reset the throws and score.

--- task ---

**Notice**: There is a space after the word 'Score: ' to separate the score from the word.

```blocks3
when I receive [score v]
change [Throws left v] by (-1)
change [Score v] by ((120) - (Landing x))
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
change [Throws left v] by (-1)
change [Score v] by ((120) - (Landing x))
set [Power v] to (0)
if <(Throws left) = (0)> then
	say (join [Score: ] (Score)) for (2) seconds
	set [Throws left v] to (3)
	set [Score v] to (0)
else
+	say [Press T for next throw] for (1) seconds
end
+stop [this script v]
```

--- /task ---

--- task ---

**Test:** Press `T` again. 

- If there are throws left, check a prompt appears to continue.
- If there are no throws left, check the score is shown and that then the throws and score are reset.

--- /task ---
