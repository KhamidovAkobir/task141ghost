Ghost ASCII Terminal
An animated, terminal-inspired ASCII portrait of Simon “Ghost” Riley from Call of Duty: Modern Warfare. Built as a lightweight, single-page website with a monochrome aesthetic, moving characters, subtle 3D-style motion, and a scrolling code-editor interface.
Features
- ASCII portrait: Converts a local Ghost image into a grid of characters rendered on an HTML canvas.
- Animated characters: Creates a dynamic terminal-like appearance rather than displaying a static photo.
- 3D-style motion: Adds depth-inspired rotation and subtle movement to the portrait.
- Interactive controls: Responds to mouse movement and touch gestures.
- Terminal UI: Includes a live-style HUD, rotation and character counters, and an auto-scrolling Python-themed code panel.
- Responsive layout: Adapts to desktop and mobile screens.
- Static hosting: Runs directly in a browser; no backend or Python installation required.
Tech Stack
- HTML5
- CSS3 and Tailwind CSS (CDN)
- Vanilla JavaScript
- HTML Canvas 2D API
- JetBrains Mono (Google Fonts)
Getting Started
Clone the repository:
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
Open index.html in a browser. For a local web server, you can also run:
python3 -m http.server 8000
Then visit http://localhost:8000.
Python is optional and is only used in the example above to serve the static files locally. The animation itself runs in JavaScript.

Project Structure
.
├── index.html       # Layout, styles, and ASCII animation logic
├── ghost_3d.jpg     # Source portrait used to generate ASCII characters
└── README.md        # Project documentation
Important: Keep ghost_3d.jpg next to index.html. The page loads it using a relative path, so changing the filename or location without updating the code may prevent the portrait from appearing.
How It Works
1. JavaScript loads ghost_3d.jpg into an offscreen canvas.
2. The image is sampled into a 112 × 84 grid.
3. Pixel brightness is mapped to ASCII characters, preserving the recognizable shapes of the mask and face.
4. Each animation frame applies depth-inspired transforms and animated character effects.
5. The browser renders the result on a visible HTML canvas, while the terminal-style interface updates around it.
This is a 2.5D visual effect, not a fully modeled 3D head. It uses a single front-facing image as its source.
Deploy to Netlify
1. Make sure index.html and ghost_3d.jpg are in the same folder.
2. Open Netlify.
3. Deploy the folder using Netlify's manual deploy option, or connect your GitHub repository for Git-based deployments.
4. Open your deployed URL to view the animation.
No build command is required for this static project.
Customization
You can edit the JavaScript in index.html to change:
- ASCII_CHARS — the characters used to draw the portrait.
- SAMPLE_W and SAMPLE_H — the sampling resolution (higher values can increase detail but also rendering cost).
- Animation timing, rotation, and character effects.
- HUD text, terminal colors, and the code panel content.
Troubleshooting
The portrait is missing: Confirm that ghost_3d.jpg exists in the deployed directory and that its name matches the image path in index.html exactly (including capitalization).

The animation looks frozen: Refresh the page and check the browser developer console for JavaScript errors.

The portrait is too small or slow: Adjust the sampling resolution and canvas sizing in index.html to suit the target device.
Credits & Disclaimer
Inspired by Simon “Ghost” Riley from Call of Duty: Modern Warfare. Character and franchise rights belong to their respective owners. This is an unofficial fan-made visual project and is not affiliated with or endorsed by Activision or the game's creators.
Made for the terminal aesthetic. Stay ghost.
