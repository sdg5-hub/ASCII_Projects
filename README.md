# ASCII Projects

A knight holding his ground. Lilies taking their time to bloom. An eye with an entire universe inside it.

A collection of animated ASCII scenes built with JavaScript, HTML5 Canvas, Python, NumPy, and Tkinter.

Each project creates moving images from colored text characters, procedural geometry, and time-based animation.

## 🎨 Projects

| Project | File | Platform | Scene |
|---------|------|----------|-------|
| ⚔️ ASCII Knight | [`knight.html`](knight.html) | Browser | An armored knight in a windswept field |
| 🌸 ASCII Lily Bouquet | [`lily.html`](lily.html) | Browser | Growing stems, unfurling leaves, and colorful blooming lilies |
| 👁️ Eye → Space | [`eye_space.py`](eye_space.py) | Python desktop | An opening eye that transitions into a starfield and heart-shaped nebula |

> GitHub displays source code. Download or clone the repository, then follow the instructions below to run each animation.

## ⚔️ ASCII Knight

A knight. A red cloak. Absolutely no intention of leaving the field.

An animated scene featuring an armored knight surrounded by swaying grass and drifting particles. Layered waves move the red fabric and cloak, while subtle breathing and swaying give the character a sense of life.

### Features

- ASCII rendering for the knight, fabric, grass, and particles.
- Flowing red fabric animated with layered waves.
- A fluttering cloak.
- Subtle breathing and body movement.
- Procedural grass with variations in height, depth, color, and motion.
- Traveling wind gusts.
- Drifting particles.
- Soft glow compositing.
- A canvas that scales to fit the browser window.
- A self-contained HTML file with no external dependencies.

No game objectives. No inventory management. Just a knight looking dramatically unavailable.

## 🌸 ASCII Lily Bouquet

Flowers made of characters. Watering is optional. Electricity is less optional.

A colorful bouquet of pink, white, yellow, orange, coral, and red lilies. Stems grow upward, leaves unfurl, and buds gradually open into layered flowers.

The bouquet sways in the wind while golden particles float through the background.

### Features

- Staggered stem growth.
- Leaves that unfurl as their stems reach them.
- Buds that swell, gain color, and bloom.
- Six-petal flowers constructed from projected 3D geometry.
- Alternating inner and outer petals with curled tips.
- Six color palettes with highlights and varying speckle patterns.
- Stamens, anthers, and central pistils.
- Leaves that droop, fold, twist, and reveal their undersides.
- Wind displacement that increases toward the top of the bouquet.
- Gentle movement in fully opened blooms.
- Floating golden particles and a faint purple background.
- Soft glow and a responsive character grid.
- A self-contained HTML file with no external dependencies.

## 👁️ Eye → Space

Look closely. Then keep looking.

A Python desktop animation that begins with an opening eye, moves through its pupil, and reveals a colorful starfield. A glowing cloud gradually takes the shape of a heart while shooting stars and a comet move through the scene.

The image is rendered as colored text inside a Tkinter window.

### Features

- Animated eyelid opening and a timed blink.
- Small gaze shifts before the zoom begins.
- A procedurally textured amber iris.
- Radial iris fibers, dark crevices, and a shaded outer edge.
- Pupil dilation and subtle movement.
- Procedural skin shading, an eyebrow, veins, and eye reflections.
- Curved upper and lower eyelashes drawn with directional characters.
- A gradual zoom through the pupil into space.
- A depth-based starfield with varied colors, brightness, and twinkling.
- Bright stars with character-based diffraction spikes.
- Shooting stars with fading directional trails.
- A slower comet with a soft tail.
- A pink nebula that gradually becomes heart-shaped.
- Gentle pulsing in the heart nebula.
- Supersampled scene rendering and bloom.
- Adaptive limits on Tkinter cell updates.
- Keyboard controls for restarting and closing the animation.

Apparently, eye contact now requires a graphics pipeline.

## 🛠️ Built With

| Technology | Role |
|------------|------|
| HTML and CSS | Browser scene structure, layout, and backgrounds |
| JavaScript | Browser animation, geometry, and rendering |
| Canvas 2D API | Character masks, image buffers, and compositing |
| Python | Desktop animation and scene logic |
| NumPy | Textures, coordinate grids, shading, and image calculations |
| Tkinter | Desktop window, text rendering, and keyboard controls |

The browser projects require no package installation.

The Python project requires NumPy and a Python installation with Tkinter support.

## 🚀 Getting Started

### Clone the repository

```bash
git clone https://github.com/sdg5-hub/ASCII_Projects.git
cd ASCII_Projects
```

Alternatively, select **Code → Download ZIP** on GitHub and extract the archive.

### Run the browser projects

Open either file in your browser:

- `knight.html`
- `lily.html`

No installation, build command, or local server is required.

If you prefer using a local server:

```bash
python3 -m http.server 8000
```

Then visit:

- Knight: http://localhost:8000/knight.html
- Lilies: http://localhost:8000/lily.html

### Run Eye → Space

Install NumPy:

```bash
python3 -m pip install numpy
```

Run the animation:

```bash
python3 eye_space.py
```

The program prints `Preparing textures...` before opening its animation window.

Tkinter must be available in your Python installation. You can check it with:

```bash
python3 -m tkinter
```

If Tkinter is missing, install the Tkinter support provided by your Python distribution or operating system.

### Eye → Space controls

| Key | Action |
|-----|--------|
| `R` | Restart the animation sequence |
| `Esc` | Close the window |

## 🎛️ Customization

Settings are defined near the top of each project's source file.

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

Additional objects define the bouquet:

- `PALETTES` — flower colors, highlights, and speckle density.
- `FLOWERS_BASE` — main flower positions, sizes, directions, colors, and timing.
- `BUDS_BASE` — bud positions, sizes, directions, maturity, and colors.
- `BUCKETS` — character groups for different brightness levels.
- `LEVELS` — brightness thresholds for those groups.

### Eye → Space settings

| Setting | What it controls |
|---------|------------------|
| `SIZE` | Tkinter font size |
| `FPS` | Target frame rate |
| `SS` | Supersampling factor |
| `ASPECT` | Window width-to-height ratio |
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
| `QL` | Number of color levels per channel |

Timing values are measured in seconds.

The bloom implementation requires supersampled grid dimensions divisible by four. Keep that constraint in mind when changing `SS` or grid dimensions.

## 🧠 How It Works

### Scene construction

**Knight:** Brightness data describes the knight, while procedural elements create fabric, grass, and particles.

**Lilies:** Curved stems and tapered leaves form the bouquet. Each flower uses six petals constructed in three dimensions, projected into two dimensions, and drawn in depth order.

**Eye → Space:** NumPy coordinate grids describe the eye and space scene. Layered noise generates textures, radial sampling creates iris fibers, and mathematical shape fields form the nebula.

### Animation

Time-based functions control movement and transitions:

- The knight uses waves for fabric, wind, and idle motion.
- The lilies use timed growth stages followed by continuous swaying.
- The eye uses opening, blinking, gaze, zoom, and nebula transformation stages.

### Character selection

Brightness determines which characters appear at each grid position.

Sparse characters represent darker areas. Denser characters represent brighter details.

Color is calculated separately, allowing the characters to carry both shape and lighting information.

### Rendering

The browser scenes use cached character masks and pixel buffers before compositing the result onto a canvas.

Eye → Space averages supersampled image data into character cells, quantizes their colors, and updates Tkinter text items. When many cells change, it prioritizes updates within an adaptive budget.

### Glow

Downsampled and blended image layers create a soft glow around bright areas.

## 📁 Project Structure

| File | Contents |
|------|----------|
| `knight.html` | Complete knight scene, styling, and animation |
| `lily.html` | Complete lily bouquet scene, styling, and animation |
| `eye_space.py` | Complete eye-to-space desktop animation |
| `README.md` | Project documentation |
| `LICENSE` | MIT license terms |

Each animation runs independently.

## ⚡ Performance Notes

Performance depends on your device, rendering dimensions, character count, and target frame rate.

### Browser scenes

- Lower `FPS` to reduce rendering frequency.
- Set `GLOW = 0` for the knight or `settings.glow = 0` for the lilies to disable glow.
- Reduce grass or particle counts in the knight scene.
- Lower `ROWS` in the lily scene to reduce grid resolution.

### Eye → Space

- Lower `MAXROWS` to reduce both rendering and text-update work.
- Lower `FPS` to reduce update frequency.
- Reduce `NS` to decrease star processing.
- Adjust `TK_MS` to change the text-update budget.

The configured frame rate is a target; actual performance depends on rendering and UI update costs.

## 💡 Possible Future Additions

- A shared project gallery
- Pause and resume controls
- Interactive settings
- Reduced-motion options
- Alternate palettes
- Screenshot and recording export
- Additional flowers and environments
- More eye colors and nebula shapes
- A browser version of Eye → Space

A horse remains outside the knight's transportation budget.

## 🤝 Contributing

Improvements, bug fixes, and creative experiments are welcome.

For larger changes, open an issue to discuss the idea first. For smaller fixes, feel free to submit a pull request.

Include a short explanation of what changed and a screenshot or recording for visual updates.

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
