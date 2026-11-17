# ⚔️ ASCII Knight

A knight. A red cloak. An unreasonable amount of wind.

An animated ASCII scene built with vanilla JavaScript and HTML5 Canvas. An armored knight stands in a windswept field while fabric ripples, grass sways, and particles drift through the air.

No game objectives. No inventory management. Just a knight holding his ground and looking dramatically unavailable.

## ✨ Features

- **ASCII rendering** — symbols create the knight, fabric, grass, and floating particles.
- **Flowing red fabric** — layered waves animate the fabric to give it a windswept appearance.
- **Animated cloak** — the loose edges shift and flutter.
- **Idle movement** — subtle breathing and swaying keep the knight from looking completely frozen.
- **Procedural grass** — blades vary in height, depth, color, and movement.
- **Traveling wind gusts** — waves of wind pass through the field.
- **Floating particles** — because standing in a field should apparently be cinematic.
- **Soft glow** — adds a little atmosphere to the scene.
- **Responsive display** — the canvas scales to fit the browser window.
- **Self-contained** — no external libraries, downloaded assets, or build tools.

## 🛠️ Built With

| Technology | Role |
| --- | --- |
| HTML | Page structure and canvas |
| CSS | Fullscreen layout and dark background |
| JavaScript | Animation, procedural movement, and rendering |
| Canvas 2D API | Drawing and compositing the scene |

No frameworks were summoned in the making of this knight.

## 🚀 Getting Started

### Run locally

1. Clone the repository:

   git clone https://github.com/sdg5-hub/Knight_HTML_ASCII.git

2. Open the project folder:

   cd Knight_HTML_ASCII

3. Open `index.html` in your browser.

That's it. No installation. No build command. The knight is already dressed and ready.

Alternatively, download the repository as a ZIP, extract it, and open `index.html`.

## 🎛️ Customization

The main settings are near the top of the script in `index.html`.

| Setting | What it controls |
| --- | --- |
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

Colors are also defined near the top of the script, including the background, armor, red fabric, and grass.

Experiment with small changes first. Increasing every setting at once may turn a peaceful field into the knight's least favorite weather forecast.

## 🧠 How It Works

### 1. Represent the knight as brightness data

The knight's silhouette and details are stored in a grid of hexadecimal brightness values. The renderer samples this grid to determine which parts of the knight appear at each position.

### 2. Animate the scene

Time-based wave functions move the fabric, cloak, grass, and particles. Breathing and swaying apply small offsets to the knight, with less movement near the feet.

He has excellent balance. It comes with the job.

### 3. Convert brightness into characters

Brightness levels map to groups of ASCII symbols. Sparse characters represent darker areas, while denser characters represent brighter areas.

Character selection stays consistent at each grid position to reduce random visual flicker.

### 4. Draw and composite

Character masks are drawn into an image buffer, then displayed on the main canvas. Smaller copies of the scene are composited back over it to create the glow effect.

### 5. Repeat

`requestAnimationFrame` schedules the animation, while a frame-rate limit controls how often the scene is rendered.

The knight continues his shift indefinitely.

## 📁 Project Structure

    Knight_HTML_ASCII/
    ├── index.html   # Complete scene, styling, and animation
    ├── README.md    # You are here
    └── LICENSE      # License terms, if included

All animation code and scene data live in `index.html`.

## ⚡ Performance Notes

The scene renders many individual characters and updates them throughout the animation. Performance depends on your device, browser, and canvas dimensions.

If the animation feels slow:

- Lower `FPS` to reduce rendering frequency.
- Set `GLOW` to `0` to disable glow compositing.
- Reduce the number of grass blades or floating particles in the script.

Lowering wind strength changes the movement, but does not significantly reduce the amount of rendering work.

## 💡 Possible Future Additions

Ideas for future development:

- Pause and resume controls
- A reduced-motion mode
- Interactive wind settings
- Alternate color palettes
- Rain, snow, or falling embers
- Screenshot export
- More ASCII characters and scenes

A horse remains outside the current transportation budget.

## 🤝 Contributing

Improvements, bug fixes, and creative experiments are welcome.

For larger changes, open an issue first to discuss the idea. For smaller fixes, feel free to submit a pull request.

Please include a short explanation of what changed and, for visual updates, a screenshot or recording.

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
