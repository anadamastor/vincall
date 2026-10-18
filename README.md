# Vincall

A 2D pixel-art alien shooter that runs in the browser. Survive 12 waves and defeat the boss.

## How to run

No install or build step is needed. The whole game is one file: `index.html`.

**Option 1: open the file**

- In Finder, double-click `index.html`, or
- In Terminal, from this folder: `open index.html`

**Option 2: local server (if the file doesn't work for any reason)**

```sh
cd /Users/ervis/Code/Projects/vincall
python3 -m http.server 8000
```

Then go to http://localhost:8000 in your browser. Press Ctrl+C in the terminal to stop the server.

## How to play

| Input | Action |
| --- | --- |
| Mouse | Aim the crosshair (the gun is invisible) |
| Click | Shoot (hold the button to fire the AR); also starts the game |
| 1 / 2 / Q | Pistol / assault rifle / switch weapon |
| R | Reload (takes 1 second, you can't shoot while reloading) |

- On the title screen, pick the starting wave with the arrow buttons or the arrow keys, then click to start.
- After a game ends, click to return to the title screen.
- Pistol: 20 bullets, 1 second reload, one shot per click.
- Assault rifle (AR): 30 bullets, 1.6 second reload, hold to fire automatically, slightly inaccurate.
- Each weapon keeps its own ammo. You have 5 lives.
- Each alien that reaches the bottom costs a life.
- There are 12 waves of 60 seconds, and each is harder than the last.
- Wave 12 has a boss. Kill it to win. If it reaches the bottom, you lose.
- Your best score is saved in the browser.

Sound starts after your first click, because browsers block audio until then.

## Menu music

To play your own recording on the title menu, save the audio file in this folder as `vincall.m4a` (next to `index.html`). It plays once each time the title menu opens (on load and when you return after a game). To use a different name or format (for example `menu.mp3` or `menu.wav`), change `MENU_SRC` near the top of the audio section in `index.html`.

Browsers don't allow sound until you interact with the page, so the first click on the title screen turns the music on, and the second click starts the game. If there is no `vincall.m4a`, the game skips this step.
