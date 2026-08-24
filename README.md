<p align="center">
  <img src="stormstack.png" width="170" alt="Stormstack">
</p>

<h1 align="center">STORMSTACK</h1>

<p align="center">
  Stack lightning photos in the browser. One HTML file, no server, nothing uploaded.
</p>

<p align="center">
  <a href="https://infinition.github.io/stormstack/"><b>Open the app</b></a>
</p>

---

## What it does

Shooting a thunderstorm gives you a burst of near identical frames, each with a bolt or two.
Stormstack layers them and blends with Lighten, which keeps only the brightest pixel of each layer.
The result is every bolt of the sequence on a single image, with the background sky untouched.

Each layer carries a mask you paint by hand. The mask lives in image coordinates, so it follows the
layer when you move or scale it.

Everything runs in the tab. Your photos never leave the machine.

## Using it

1. Drop your photos anywhere on the page, or click **+ Import**.
2. The first layer stays Normal, the ones above switch to **Lighten**. The ⚡ button forces every
   layer above the base into that mode.
3. Align the layers: drag the image on the canvas, pull a **corner handle** to scale, or type exact
   values in the panel.
4. **Erase** removes an area of the active layer, a stray bolt or a reflection. **Restore** brings it
   back. Hardness and flow shape the brush edge.
5. **Export PNG**.

### Snapping

While dragging or resizing, layers snap to the document edges and centre, and to the edges and
centres of the other layers. Resizing also snaps to 100 %, contain, cover, width and height.
Red guides show what caught. Hold `Alt` to suspend it, or toggle the **Snap** button.

### Fitting

Per layer and for the whole stack: `Contain`, `Cover`, `Width`, `Height`, `1:1`, `Center`.
Useful when the frames do not all come from the same body or the same crop.

### Fine control

Opacity, scale, X and Y each have a slider, a direct input field and fine steps. X and Y move one
pixel at a time with `+1` / `-1`, ten with `+10` / `-10`, and with the arrow keys.

## Languages

English by default, French available. The `EN` / `FR` buttons in the header switch instantly and the
choice is remembered. All strings live in a single `I18N` table, so adding a language means adding
one entry.

## Shortcuts

| Key | Action |
| --- | --- |
| `V` | Move |
| `E` | Erase |
| `R` | Restore |
| `S` | Toggle snapping |
| `Alt` (held) | Suspend snapping |
| `[` `]` | Brush size |
| Arrows | Move layer by 1 px (10 px with `Shift`) |
| `F` | Fit view |
| `Esc` | Close the layer panel |
| `Ctrl` + `Z` | Undo |
| `Ctrl` + `Shift` + `Z` | Redo |
| Wheel | Zoom |
| Space or right click | Pan |

## Phone and tablet

The interface adapts to touch: larger targets, collapsible layer panel, bigger resize handles, and
margins that respect display cutouts.

- One finger: active tool.
- Two fingers: zoom and pan.
- Tapping outside the layer panel closes it.

On iOS, `Share → Add to Home Screen` installs it fullscreen. On export the PNG opens in a tab:
`Share → Save to Photos`.

## Formats and limits

Supported formats are whatever the browser decodes: JPEG, PNG, WebP, AVIF, TIFF, GIF, BMP.

**HEIC** is not decodable by any desktop browser. If your photos come from an iPhone, set
`Settings → Camera → Formats → Most Compatible`, or convert them to JPEG. The app detects the case
and says so.

Working resolution is capped to fit in canvas memory, which is tight on iOS. The **Working** setting
runs from 2048 px to full resolution and applies to subsequent imports. If export fails for lack of
memory, lower it.

## Running locally

No dependencies, no build step. Download `index.html` and open it. The file is self contained,
icons included, and works offline.

## License

MIT.
