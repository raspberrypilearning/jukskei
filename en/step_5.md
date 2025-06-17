## Challenge

### Add a celebration!

--- task ---

Select the **Hat** sprite. ![The Hat sprite](images/Hat.png){ width: 200px; }

--- /task ---

--- task ---

Show the hat and play a sound on a high score.

```blocks3
+when I receive [score v]
+forever
	if <(Score) > (200)> then
    	show                              	// Try changing this score
    	play sound [Dubstep v] until done 	// You can change the sound
	end
end
```

--- /task ---

--- task ---

Add reset code.

```blocks3
+when [n v] key pressed
+hide
```

--- /task ---

--- task ---

**Test:** Press `n` and play to a score above 200 - check the hat shows and you hear your chosen sound!

--- /task ---

### Add a controls screen

--- task ---

Select the Stage, duplicate the Hill backdrop and rename it ‘Controls’.

--- /task ---

--- task ---

Add text to the Controls backdrop to show how to control the game.

--- /task ---

--- task ---

Add this single block of code to the ‘when n key pressed’ script.

```blocks3
when [n v] key pressed
stop all sounds
set [Score v] to [0]
set [Power v] to [0]
set [Throws left v] to [3]
+switch backdrop to [Hill v]
show variable [Power v]
show variable [Score v]
show variable [Throws left v]
```

--- /task ---

### Choose a different Player sprite

--- task ---

Choose the Player sprite and select a new sprite from the library, paint your own, upload an image, or select a random one.

--- /task ---

--- task ---

Make sure your new sprite has two costumes: 'throw' and 'still' to keep the throwing animation.

--- /task ---
