# Ascii Flower Bouquet

A spinning 3D flower bouquet that runs right in your terminal. Daisies, tulips, a paper wrap with a ribbon, baby's breath, sparkles, and floating hearts. All drawn with text characters.

Saw it on TikTok? This is the code.

<p align="center">
  <img src="screenshot.png" alt="bouquet3d running in a terminal" width="600">
</p>

## Run it

You just need Python 3. No packages to install.

```bash
git clone https://github.com/YOUR_USERNAME/bouquet3d.git
cd bouquet3d
python3 bouquet3d.py
```

On Windows use `python bouquet3d.py` instead.

Press `Ctrl+C` to stop it.

## Tips

- Make your terminal window big, or zoom out a bit (`Ctrl -` / `Cmd -`). More space means a smoother looking bouquet.
- Use a terminal that supports 256 colors. Most do: macOS Terminal, iTerm2, Windows Terminal, VS Code, and pretty much anything on Linux.
- If the hearts show up as weird boxes, switch your terminal font to something with good Unicode support.

## Make it yours

Open `bouquet3d.py` and change the values at the top:

| Setting | What it does |
| --- | --- |
| `MESSAGE` | The text under the bouquet. Put their name in here. |
| `SPIN_SPEED` | How fast it spins |
| `TILT` | How much you look down at it |
| `CAM_DIST` | Lower number = more dramatic perspective |
| `NUM_HEARTS` | How many hearts float in the background |
| `FPS` | Frame rate |

You can also swap the color lists (`PINK`, `RED`, `PURPLE`, etc.) to change the flowers. They're 256-color terminal codes.

## How it works

Every part of the bouquet is a set of 3D points. Each frame the points get rotated, projected onto the screen with perspective, and shaded based on a light direction. A depth buffer makes sure the closest thing wins each character spot. The flower heads are drawn as flat shapes that always face you so the petals stay readable while it spins.

---

Follow me on TikTok [@alishsharma](https://www.tiktok.com/@alishsharma) for more terminal stuff.
