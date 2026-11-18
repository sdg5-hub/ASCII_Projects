# ASCII Projects

A knight holding his ground. Lilies taking their time to bloom. An unreasonable amount of wind.

Animated ASCII scenes built with vanilla JavaScript and HTML5 Canvas. Each project turns characters into a colorful, moving scene using procedural animation and pixel-based rendering.

No frameworks, external libraries, or downloaded assets. Just HTML files you can open in your browser.

## 🎨 Projects

| Project | File | Scene |
|---------|------|-------|
| ⚔️ ASCII Knight | [`knight.html`](knight.html) | An armored knight in a windswept field with flowing red fabric, animated grass, and drifting particles |
| 🌸 ASCII Lily Bouquet | [`lily.html`](lily.html) | A colorful bouquet with growing stems, unfurling leaves, blooming lilies, and floating golden particles |

> GitHub displays HTML source code. To view an animation, download the files and open the corresponding HTML file in your browser.

## ⚔️ ASCII Knight

A knight. A red cloak. Absolutely no intention of leaving the field.

An animated ASCII scene featuring an armored knight surrounded by swaying grass and drifting particles. Layered waves move the red fabric and cloak, while subtle breathing and swaying keep the knight from looking completely frozen.

### Features

- **ASCII rendering** — characters form the knight, fabric, grass, and particles.
- **Flowing red fabric** — layered waves create continuous movement.
- **Animated cloak** — loose edges shift and flutter in the wind.
- **Idle movement** — breathing and swaying add subtle motion.
- **Procedural grass** — blades vary in height, depth, color, and movement.
- **Traveling wind gusts** — waves of wind move through the field.
- **Floating particles** — a little extra atmosphere.
- **Soft glow** — compositing adds light around the scene.
- **Responsive display** — the canvas scales to fit the browser window.

No game objectives. No inventory management. Just a knight looking dramatically unavailable.

## 🌸 ASCII Lily Bouquet

Flowers, except every petal is made of characters and none of them need watering.

An animated ASCII bouquet featuring pink, white, yellow, orange, coral, and red lilies. Stems grow upward, leaves unfurl as the stems reach them, and flowers gradually open into layered blooms.

The bouquet sways in the wind while golden particles drift upward through the background.

### Features

- **Growing stems** — staggered growth brings the bouquet into view.
- **Unfurling leaves** — leaves open as their stems grow past their attachment points.
- **Blooming flowers** — buds swell, gain color, and gradually open.
- **3D petal geometry** — petals are constructed in three dimensions and projected onto the canvas.
- **Six-petal blooms** — alternating inner and outer petals form each lily.
- **Multiple color palettes** — six flower colors with different shading and speckle patterns.
- **Curled petal tips** — petals bend backward as the flowers open.
- **Flower details** — stamens, anthers, and a central pistil appear during blooming.
- **Natural leaf shapes** — leaves droop, fold, and twist to reveal their undersides.
- **Wind animation** — higher parts of the bouquet sway more strongly.
- **Gentle bloom movement** — open flowers subtly expand and contract.
- **Floating golden particles** — firefly-like points rise around the bouquet.
- **Soft glow** — downscaled image layers create a diffuse lighting effect.
- **Responsive layout** — the character grid adapts to the window proportions.

A bouquet with a slightly more demanding relationship with your CPU than a normal bouquet.

## 🛠️ Built With

| Technology | Role |
|------------|------|
| HTML | Page structure and canvas |
| CSS | Fullscreen layout and dark background |
| JavaScript | Scene construction, animation, and rendering |
| Canvas 2D API | Character masks, image buffers, and compositing |
| Typed arrays | Brightness, color, and pixel data |
| `requestAnimationFrame` | Scheduling animation frames |

Each scene is self-contained in its own HTML file.

## 🚀 Getting Started

### Clone the repository

```bash
git clone https://github.com/sdg5-hub/ASCII_Projects.git
cd ASCII_Projects
```

### Open a scene

Open either file directly in your browser:

- `knight.html`
- `lily.html`

No installation or build command is required.

Alternatively, select **Code → Download ZIP** on GitHub, extract the archive, and open either HTML file.

### Optional: Run a local server

If you prefer serving the files locally and have Python installed:

```bash
python3 -m http.server 8000
```

Then visit:

- Knight: http://localhost:8000/knight.html
- Lilies: http://localhost:8000/lily.html

## 🎛️ Customization

Edit the settings near the top of each file's script, save the file, and refresh your browser.

### Knight settings

| Setting | What it controls |
|---------|------------------|
| `LOOP` | Duration of the main fabric animation cycle |
| `WAVE` | Strength of the fabric waves |
| `GLOW` | Intensity of the soft glow |
| `BREATH` | Amount of vertical breathing movement |
| `SWAY` | Amount of side-to-side movement |
| `CLOAK` | Strength of the cloak's flutter |
| `GRASS_WIND` | Wind strength affecting the grass |
| `GRASS_HEIGHT` | Grass height multiplier |
| `HORIZON` | Vertical position of the field's horizon |
| `FONT_SIZE` | Size of the rendered characters |
| `FPS` | Target rendering frame rate |

Colors for the background, armor, red fabric, and grass are also defined in the script.

### Lily settings

| Setting | What it controls |
|---------|------------------|
| `FONT_SIZE` | Size of the rendered characters |
| `FPS` | Target rendering frame rate |
| `ROWS` | Number of rows in the character grid |
| `WAVE_PERIOD` | Base period used by the wave functions |
| `BREATH` | Duration of the gentle bloom movement cycle |
| `BREATH_DEPTH` | How much open flowers contract during that cycle |
| `settings.wind` | Strength of the bouquet's swaying |
| `settings.size` | Size multiplier for the main flowers |
| `settings.glow` | Intensity of the glow effect |
| `STEM_DUR` | Duration of stem growth in seconds |

Additional scene data:

| Object | Purpose |
|--------|---------|
| `PALETTES` | Flower colors, highlights, and speckle density |
| `FLOWERS_BASE` | Main flower positions, sizes, directions, colors, and bloom timing |
| `BUDS_BASE` | Bud positions, sizes, directions, maturity, and colors |
| `BUCKETS` | Character groups used for different brightness levels |
| `LEVELS` | Brightness thresholds for selecting character groups |

Try small changes first. Maximum wind and maximum flower size may produce a bouquet with strong opinions.

## 🧠 How It Works

Both projects follow the same general rendering approach: construct a scene, animate its properties, convert brightness into characters, and draw the result.

### 1. Construct the scene

**Knight:** A grid of hexadecimal brightness values describes the knight's silhouette and details. Additional drawing logic builds the surrounding fabric, grass, and particles.

**Lilies:** Curved stems and tapered leaves form the bouquet. Each flower uses six petals built from 3D geometry, projected into two dimensions and drawn from back to front.

### 2. Animate with time

Wave functions create wind, fabric movement, breathing, and swaying.

The lily scene also uses timed growth stages:

1. Stems grow upward.
2. Leaves unfurl as the stems reach them.
3. Buds appear and swell.
4. Flowers gain color and open.
5. Open blooms continue moving gently in the breeze.

### 3. Map brightness to characters

Each cell in the scene stores brightness and color information.

Brightness selects a group of ASCII characters. Sparse symbols represent darker areas, while denser symbols represent brighter areas.

### 4. Render character masks

Characters are rendered into reusable masks. The renderer combines those masks with the scene's color data to write pixels into an image buffer.

This creates the appearance of a picture assembled from colored text.

### 5. Composite the glow

Smaller copies of the rendered scene are enlarged and blended over the original to create a soft glow.

### 6. Draw the next frame

`requestAnimationFrame` schedules updates, while an FPS limit controls how frequently the scene is rendered.

The knight continues his shift. The flowers continue being flowers.

## 📁 Project Structure

- **`knight.html`** — Complete knight scene, styling, settings, and animation.
- **`lily.html`** — Complete lily bouquet scene, styling, settings, and animation.
- **`README.md`** — Project documentation.
- **`LICENSE`** — MIT license terms.

Each HTML file runs independently.

## ⚡ Performance Notes

These scenes update many character cells and pixels throughout the animation. Performance depends on your device, browser, and rendering dimensions.

If an animation feels slow:

- Lower `FPS` to reduce rendering frequency.
- Disable glow with `GLOW = 0` for the knight or `settings.glow = 0` for the lilies.
- Reduce grass or particle counts in the knight scene.
- Lower `ROWS` in the lily scene to reduce the character grid resolution.

Reducing wind strength changes the movement but does not significantly reduce rendering work.

## 💡 Possible Future Additions

- Pause and resume controls
- Replay controls for the lily growth sequence
- A reduced-motion mode
- Interactive settings
- Alternate color palettes
- Screenshot export
- Rain, snow, or falling embers
- Additional flowers and ASCII scenes
- A shared gallery page

A horse remains outside the current transportation budget.

## 🤝 Contributing

Improvements, bug fixes, and creative experiments are welcome.

For larger changes, open an issue to discuss the idea first. For smaller fixes, feel free to submit a pull request.

Include a short explanation of what changed and, for visual updates, a screenshot or recording.

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
