## The skey sprite

--- task ---

Select the **Skey** sprite. ![The Skey sprite](images/Skey.png){:width="100px"}

--- /task ---

### Move to the peg

Set the initial position of the skey.

--- task ---

```blocks3
+when I receive [throw v]
+go to x: (-127) y: (29)
+set rotation style [all around v]
+point towards (Peg v)
+start sound (Siren Whistle v)
```

--- /task ---

Arc the skey through the air.

--- task ---

```blocks3
when I receive [throw v]
go to x: (-127) y: (29)
set rotation style [all around v]
point towards (Peg v)
start sound (Siren Whistle v)
+repeat until <(distance to (Peg v)) < (Landing x)> // < means 'less than'
  turn cw (15) degrees
  move (10) steps
  point towards (Peg v)
end
+start sound (Whistle Thump v)
+wait (0.5) seconds
```

--- /task ---

--- task ---

**Test:** Press `T'. Check the skey moves through the air in an arc and that throwing and landing sounds play.

--- /task ---

### Reset

Reset the position of the skey after it lands.

--- task ---

```blocks3
when I receive [throw v]
go to x: (-127) y: (29)
set rotation style [all around v]
point towards (Peg v)
start sound (Siren Whistle v)
repeat until <(distance to (Peg v)) < (Landing x)>
  turn cw (15) degrees
  move (10) steps
  point towards (Peg v)
end
start sound (Whistle Thump v)
wait (0.5) seconds
+go to x: (-136) y: (-11)
+point in direction (120)
```

--- /task ---

### Trigger scoring

Add a broadcast message to trigger scoring.

--- task ---

```blocks3
when I receive [throw v]
go to x: (-127) y: (29)
set rotation style [all around v]
point towards (Peg v)
start sound (Siren Whistle v)
repeat until <(distance to (Peg v)) < (Landing x)>
  turn cw (15) degrees
  move (10) steps
  point towards (Peg v)
end
start sound (Whistle Thump v)
wait (0.5) seconds
go to x: (-136) y: (-11)
point in direction (120)
+broadcast (score v)
```

--- /task ---
