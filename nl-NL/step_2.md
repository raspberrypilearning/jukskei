## Player

\--- task ---

Open the [starter project](https://scratch.mit.edu/projects/1187059894/editor/){:target="_blank"}.

\--- /task ---

The starter project contains some starter code and all the sprites you need.

\--- task ---

Select the **Player** sprite. ![The Player sprite](images/Player.png){:width="100px"}

\--- /task ---

### Throw!

Animate the Player when they throw a skey.

\--- task ---

In the `when I receive`{:class="block3events"} block, switch the costume.

```blocks3
+when I receive [throw v]
+switch costume to [throw v]
+wait (1) seconds
+switch costume to [still v]
```

\--- /task ---

\--- task ---

**Test:**

- Press `n` to start a new game, then `t` to start a new throw - check the power bar cycles from 0 to 100.

- Press `space` to stop the power bar -  check the player changes costume to the throw costume and then returns back to the still costume

\--- /task ---
