# ASCII Projects

A knight holding his ground. Lilies taking their time to bloom. An eye containing a universe. A black hole making everything unnecessarily dramatic.

A collection of animated ASCII scenes for the browser and desktop. Each project uses colored text characters, procedural geometry, and time-based animation to create a moving scene.

## 🎨 Projects

| Project | File | Runs In | Scene |
|---------|------|---------|-------|
| ⚔️ ASCII Knight | [`knight.html`](knight.html) | Browser | An armored knight in a windswept field |
| 🌸 ASCII Lily Bouquet | [`lily.html`](lily.html) | Browser | Growing stems, unfurling leaves, and blooming lilies |
| 👁️ Eye → Space | [`eye_space.py`](eye_space.py) | Tkinter window | An opening eye that transitions into a starfield and heart-shaped nebula |
| 🌌 ASCII Black Hole | [`black_hole.py`](black_hole.py) | Pygame window | A glowing accretion disk surrounding a dark central shadow |

> GitHub displays source code. Clone or download the repository, then follow the instructions below to run an animation.

## ⚔️ ASCII Knight

A knight. A red cloak. Absolutely no intention of leaving the field.

An animated scene featuring an armored knight surrounded by swaying grass and drifting particles. Layered waves move the red fabric and cloak, while subtle breathing and swaying keep the character from looking completely frozen.

### Features

- ASCII rendering for the knight, fabric, grass, and particles.
- Flowing red fabric animated with layered waves.
- A fluttering cloak.
- Subtle breathing and body movement.
- Procedural grass with varied height, depth, color, and motion.
- Traveling wind gusts.
- Drifting particles.
- Soft glow compositing.
- A canvas that scales to fit the browser window.
- A self-contained HTML file with no external dependencies.

No game objectives. No inventory management. Just a knight looking dramatically unavailable.

## 🌸 ASCII Lily Bouquet

Flowers made of characters. No watering schedule required.

A bouquet of pink, white, yellow, orange, coral, and red lilies. Stems grow upward, leaves unfurl, and buds gradually open into layered flowers.

The bouquet sways in the wind while golden particles float through the background.

### Features

- Staggered stem growth.
- Leaves that unfurl as their stems reach them.
- Buds that swell, gain color, and bloom.
- Six-petal flowers constructed from projected 3D geometry.
- Alternating inner and outer petals with curled tips.
- Six color palettes with highlights and varying speckle patterns.
- Stamens, anthers, and central pistils.
- Leaves that droop, fold, and twist.
- Wind movement that increases toward the top of the bouquet.
- Gentle movement in fully opened blooms.
- Floating golden particles and a faint purple background.
- Soft glow and a responsive character grid.
- A self-contained HTML file with no external dependencies.

## 👁️ Eye → Space

Look closely. Then keep looking.

A Python desktop animation that begins with an opening eye, moves through its pupil, and reveals a starfield. A glowing pink cloud gradually becomes a heart-shaped nebula while shooting stars and a comet move through the scene.

The image is rendered as colored text inside a Tkinter window.

### Features

- Animated eyelid opening and a timed blink.
- Small gaze shifts before the zoom begins.
- A procedurally textured amber iris.
- Radial iris fibers, dark crevices, and a shaded outer edge.
- Changing pupil size.
- Procedural skin shading, an eyebrow, veins, and reflections.
- Curved upper and lower eyelashes drawn with directional characters.
- A gradual zoom through the pupil into space.
- A depth-based starfield with varied colors, brightness, and twinkling.
- Bright stars with character-based light spikes.
- Shooting stars with fading trails.
- A slower comet with a soft tail.
- A pink nebula that gradually becomes heart-shaped.
- Gentle pulsing in the heart nebula.
- Supersampled rendering and bloom.
- Adaptive limits on Tkinter text updates.
- Restart and exit controls.

Apparently, eye contact now requires a graphics pipeline.

## 🌌 ASCII Black Hole

A dark center. A bright disk. Several excellent reasons to admire it from a distance.

A Python and Pygame animation that builds a black hole scene in stages. A thin ring draws itself, a surrounding glow develops, and an accretion disk spreads outward before a bright flash reveals its full structure.

Orbiting gas patterns and bright pulses move through the disk and a curved halo above the shadow. A small camera movement accompanies the flash.

This is a stylized visual effect using procedural shapes and shading, rather than a physical ray-tracing simulation.

### Features

- A ring that progressively draws itself around the central shadow.
- A softly changing aura.
- A tilted accretion disk with layered gas streaks.
- Faster orbital movement toward the inner disk.
- A curved halo suggesting gravitational lensing.
- Bright pulses traveling along selected gas rings.
- A timed flash and expanding shock ring.
- A camera zoom and changing disk viewing angle.
- Red, orange, amber, and pale hot highlights.
- Background stars and a faint dust lane.
- Directional characters along the initial ring.
- Cached character masks and array-based color rendering.
- Fading frame trails.
- Two additive glow layers.
- A window that scales down for smaller displays.
- A status display showing time, spin, peak heat, and character count.
- A repeating 20-second sequence.
- Pause, restart, screenshot, and exit controls.

The source includes an on-screen signature: `@jin_22ee · 2026`.

## 🛠️ Built With

| Technology | Role |
|------------|------|
| HTML and CSS | Browser page structure and fullscreen layout |
| JavaScript | Browser animation, geometry, and rendering |
| Canvas 2D API | Character masks, image buffers, and compositing |
| Python | Desktop scene logic and animation |
| NumPy | Coordinate grids, textures, shading, and image calculations |
| Tkinter | Eye → Space window and text rendering |
| Pygame | Black hole window, character rendering, glow, and input |

The browser projects require no package installation.

The Python projects require NumPy. The black hole also requires Pygame, and Eye → Space requires a Python installation with Tkinter support.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/sdg5-hub/ASCII_Projects.git
cd ASCII_Projects
```

If you already cloned it, update your local copy:

```bash
cd ~/ASCII_Projects
git pull
```

Alternatively, select **Code → Download ZIP** on GitHub and extract the archive.

### 2. Run the browser projects

Open either HTML file in your browser:

- `knight.html`
- `lily.html`

On macOS:

```bash
open knight.html
open lily.html
```

No installation, build command, or local server is required.

### 3. Set up the Python projects

From the repository folder, create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

On Windows PowerShell, activate it with:

```powershell
.venv\Scripts\Activate.ps1
```

Install the Python dependencies:

```bash
python -m pip install numpy pygame
```

### 4. Run a Python animation

Eye → Space:

```bash
python eye_space.py
```

ASCII Black Hole:

```bash
python black_hole.py
```

Eye → Space prints `Preparing textures...` before opening its window.

If a command reports that the file does not exist, check the filenames in your local repository and confirm that you have pulled the latest changes.

### Running again later

Activate the existing environment whenever you open a new terminal:

```bash
cd ~/ASCII_Projects
source .venv/bin/activate
python black_hole.py
```

Replace `black_hole.py` with `eye_space.py` to run the eye animation.

You only need to create the environment and install dependencies once, unless you remove or recreate it.

### Tkinter availability

Check whether your Python installation includes Tkinter:

```bash
python -m tkinter
```

If it is unavailable, install the Tkinter support supplied by your Python distribution or operating system.

### Optional local web server

To serve the browser projects locally:

```bash
python3 -m http.server 8000
```

Then visit:

- Knight: http://localhost:8000/knight.html
- Lilies: http://localhost:8000/lily.html

## ⌨️ Controls

### Eye → Space

| Key | Action |
|-----|--------|
| `R` | Restart the sequence |
| `Esc` | Close the window |

### ASCII Black Hole

| Key | Action |
|-----|--------|
| `Space` | Pause or resume |
| `R` | Reset the sequence to its beginning |
| `S` | Save a PNG screenshot beside the Python script |
| `Esc` | Close the window |

The black hole sequence also restarts automatically after 20 seconds. Resetting while paused keeps the animation paused; press `Space` to continue.

Screenshots use filenames such as `black_hole_1794950000.png`.

## 🎛️ Customization

Edit settings in the source file, save, and restart the animation or refresh the browser.

### Knight settings

| Setting | What it controls |
|---------|------------------|
| `LOOP` | Main fabric animation cycle duration |
| `WAVE` | Fabric wave strength |
| `GLOW` | Glow intensity |
| `BREATH` | Vertical breathing movement |
| `SWAY` | Side-to-side movement |
| `CLOAK` | Cloak flutter strength |
| `GRASS_WIND` | Wind movement in the grass |
| `GRASS_HEIGHT` | Grass height multiplier |
| `HORIZON` | Field horizon position |
| `FONT_SIZE` | Character size |
| `FPS` | Target frame rate |

### Lily settings

| Setting | What it controls |
|---------|------------------|
| `FONT_SIZE` | Character size |
| `FPS` | Target frame rate |
| `ROWS` | Character grid height |
| `WAVE_PERIOD` | Base wave period |
| `BREATH` | Bloom movement cycle duration |
| `BREATH_DEPTH` | Amount of bloom contraction |
| `settings.wind` | Bouquet sway strength |
| `settings.size` | Main flower size multiplier |
| `settings.glow` | Glow intensity |
| `STEM_DUR` | Stem growth duration |

Additional scene data:

- `PALETTES` — flower colors, highlights, and speckle density.
- `FLOWERS_BASE` — main flower positions, sizes, directions, colors, and timing.
- `BUDS_BASE` — bud positions, sizes, directions, maturity, and colors.
- `BUCKETS` — character groups for different brightness levels.
- `LEVELS` — brightness thresholds for selecting those groups.

### Eye → Space settings

| Setting | What it controls |
|---------|------------------|
| `SIZE` | Tkinter font size |
| `FPS` | Target frame rate |
| `SS` | Supersampling factor |
| `ASPECT` | Window aspect ratio |
| `MAXROWS` | Maximum character grid height |
| `TK_MS` | Target time budget for text updates |
| `T_OPEN` | Eye opening start time |
| `T_OPEN_D` | Eye opening duration |
| `T_BLINK` | Blink start time |
| `T_Z0` | Zoom start time |
| `T_ZD` | Zoom duration |
| `ZEND` | Base zoom endpoint |
| `T_HEART` | Heart transformation start time |
| `T_HEART_D` | Heart transformation duration |
| `NS` | Number of star particles |
| `RAMP` | Characters ordered by visual density |
| `QL` | Color levels per channel |

The bloom implementation requires supersampled grid dimensions divisible by four. Preserve that constraint when changing `SS` or grid dimensions.

### Black hole settings

| Setting | What it controls |
|---------|------------------|
| `LOOP` | Sequence duration before automatic restart |
| `R0` | Central shadow radius relative to frame height |
| `TILT` | Disk rotation in the image |
| `INC` | Initial apparent disk thickness |
| `R_IN` | Inner disk radius |
| `R_OUT` | Outer disk radius |
| `FLASH` | Flash timing |
| `POOLS` | Character groups for different heat levels |
| `TAG_COLOR` | Colors for gas, stars, and dust |
| `CW`, `CH` | Character cell width and height |
| `FONT_PX` | Font size |
| `W`, `H` | Internal rendering dimensions |
| `TRAIL` | Fraction of the previous trail image retained each frame |
| `TITLE` | Window title |
| `SIGN` | On-screen signature |

The frame-rate target is set by `clock.tick(30)` in the main loop. Glow strengths are set in the two `glow_layer(...)` calls.

Timing values are measured in seconds.

## 🧠 How It Works

### Construct the scene

- **Knight:** Brightness data describes the character, with procedural fabric, grass, and particles around it.
- **Lilies:** Curves form stems and leaves. Six projected 3D petals form each flower.
- **Eye → Space:** NumPy grids describe the eye, iris, pupil, starfield, and nebula.
- **Black Hole:** Radial and elliptical fields describe the shadow, disk, halo, and glow. Angular patterns create the appearance of orbiting gas.

### Animate with time

Wave functions and eased transitions control movement.

The browser scenes use wind, breathing, growth, and bloom cycles. Eye → Space follows a timed opening and zoom sequence. The black hole builds its ring, aura, disk, flash, and orbital highlights over a repeating timeline.

### Select characters and colors

Brightness or heat determines which characters appear at each grid position.

Sparse characters represent darker areas; denser characters represent brighter details. Color adds shading, highlights, and atmosphere.

### Render the image

The browser projects use cached character masks and pixel buffers.

Eye → Space converts supersampled image data into colored Tkinter text cells and prioritizes updates within an adaptive budget.

The black hole uses a cached glyph atlas, NumPy arrays, and Pygame surfaces to assemble and tint the character grid.

### Add glow

Scaled image layers create diffuse light around bright regions. The black hole also retains a fading image of earlier frames to create trails.

## 📁 Project Structure

| File | Contents |
|------|----------|
| `knight.html` | Knight browser animation |
| `lily.html` | Lily bouquet browser animation |
| `eye_space.py` | Eye-to-space Tkinter animation |
| `black_hole.py` | Black hole Pygame animation |
| `README.md` | Project documentation |
| `LICENSE` | Repository license terms |

Each animation runs independently.

## ⚡ Performance Notes

Performance depends on your device, rendering dimensions, character count, and frame-rate target.

### Browser projects

- Lower `FPS`.
- Disable glow using `GLOW = 0` for the knight or `settings.glow = 0` for the lilies.
- Reduce grass or particle counts in the knight scene.
- Lower `ROWS` in the lily scene.

### Eye → Space

- Lower `MAXROWS`.
- Lower `FPS`.
- Reduce `NS` to process fewer stars.
- Adjust `TK_MS` to change the text-update budget.

### ASCII Black Hole

- Reduce `W` and `H` to render a smaller scene.
- Increase character cell dimensions to reduce the grid size.
- Lower the target in `clock.tick(30)`.
- Reduce or remove glow passes.

The black hole renders at its internal resolution even when its window is scaled down. A smaller displayed window alone does not reduce the underlying rendering workload.

## 💡 Possible Future Additions

- A shared gallery page
- Interactive customization
- Reduced-motion options
- More browser playback controls
- Alternate palettes
- Recording export
- Additional flowers and environments
- More nebula shapes
- A browser version of the Python scenes

A horse remains outside the knight's transportation budget.

## 🤝 Contributing

Improvements, bug fixes, and creative experiments are welcome.

For larger changes, open an issue to discuss the idea first. For smaller fixes, feel free to submit a pull request.

Include a short explanation of what changed and a screenshot or recording for visual updates.

## 📄 License and Credits

See [LICENSE](LICENSE) for the repository's license terms.

Preserve applicable attribution and license notices for any third-party code included in the collection. The black hole source currently displays the signature `@jin_22ee · 2026`; that signature alone does not establish its license.
