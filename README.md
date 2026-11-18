# GOVNOJED 💩

A satirical side-scrolling browser game about the pro-government propaganda machine in Serbia. Run, jump, collect what you are fed, and dodge what the people throw at you.

### ▶ [Play the live demo](https://pumpajjj.github.io/govnojed/)

[![GOVNOJED](assets/social.png)](https://pumpajjj.github.io/govnojed/)

## How to play

Start the game with **Space**, **Enter**, any arrow key, or by tapping **Press Start**.

| Action | Keyboard | Touch / mouse |
| --- | --- | --- |
| Move left / right | ← / → | Tap left or right of the character |
| Jump | Space or ↑ | Tap the character |
| Restart after game over | R | Tap "Press R to Restart" |

You start with 3 lives (💰). Items scroll in along the ground:

| Item | Effect |
| --- | --- |
| 💩 Poo | +1 score |
| 🐂 Ox | Speed boost for 5 seconds |
| 💵 Money | +1 life (rare) |
| 🚽 Toilet | Slow motion for 5 seconds |
| Pump, fist, egg, horse | −1 life |

Each pickup triggers a speech bubble with a random line. The game ends when you run out of lives. Your high score is saved in the browser (`localStorage`).

Press **D** to toggle debug view.

## Tech

- [Phaser 3](https://phaser.io/), loaded from the jsDelivr CDN
- A single `index.html` with three scenes: start screen, game and game over
- Parallax background and foreground layers
- Sprites packed into a texture atlas (`assets/govnojed.png` + `assets/govnojed.json`)

No build step and no dependencies to install.

## Run locally

```sh
git clone https://github.com/pumpajjj/govnojed.git
cd govnojed
python3 -m http.server 8000
```

Then open <http://localhost:8000>. A local server is needed because Phaser loads the assets over HTTP; opening `index.html` directly from disk will not work.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole game: scenes, logic and styles |
| `assets/bg.png`, `assets/fg.png` | Parallax background and foreground |
| `assets/char-running.png`, `assets/char-jumping.png` | Character sprite sheets |
| `assets/items.png` | Item sprites |
| `assets/govnojed.png`, `assets/govnojed.json` | Texture atlas (title, buttons, items) |
| `assets/social.png` | Social media preview image |

## Deployment

Hosted on GitHub Pages from the repository root. Push to the default branch and the site updates.

## Related

- [PUMPAJJJ!](https://pumpajjj.github.io/pumpajjj/): pump up the balloons and support the students

## Contributing

Issues and pull requests are welcome.
