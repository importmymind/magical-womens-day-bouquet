# Magical Women's Day Bouquet 🌸✨

A beautifully designed, interactive "Build Your Own Bouquet" web application crafted specifically for International Women's Day. This project features a fully responsive, mobile-first design with a magical aesthetic, dynamic flower arrangement algorithms, and native sharing capabilities.

## 🌟 Features

- **Interactive Bouquet Editor:** Users can select from a variety of beautifully illustrated flower assets to build their custom bouquet.
- **Florist-Grade Sorting Algorithm:** A sophisticated 3D-tier overlapping algorithm calculates specific angles (`[0, 15, -15, 8, -8...]`) and dynamic stem heights. This ensures flowers fan out gracefully without awkward wide gaps or completely covering the front faces of previous flowers.
- **Magical UI/UX:** 
  - Dynamic floating background particles and a gently pulsing soft-glow heart frame in the landing area.
  - Frost-glass (Glassmorphism) UI elements resembling a modern hatbox vase.
  - Elegant typography featuring Google Fonts (`Pinyon Script`, `Great Vibes`, `Playfair Display`).
- **Smooth Mobile-First Carousel:** The bottom flower menu utilizes a custom scrollable carousel (`touch-action`) with sleek minimalistic scrollbars, bound cleanly within a `600px` max-width container on desktops.
- **Export & Share Generation:**
  - **Save Image:** Fully integrated with `html2canvas` to render the user's customized bouquet directly to their device gallery (`My-Bouquet.png`) with one click across all platforms.
  - **Sharable Links:** Safely encodes the exact sequence of added flowers directly into the URL query parameters (`?b=1-4-2...`).
  - **QR Code Engine:** Instantly generates a clean, centered QR Code using `qrcode.js` that points to the user's specific bouquet URL.
- **Single File Architecture:** Zero complex build tools. The entire application (HTML, CSS, JS) is neatly bundled into a single extremely performant `index.html` file.

## 🚀 Live Demo & Usage

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/importmymind/magical-womens-day-bouquet.git
   ```

2. **Setup:**
   Place your flower assets (`flower1.png`, `flower2.png`, ...) inside the `assets/` folder in the root directory.

3. **Run:**
   Simply open `index.html` in any modern web browser. No server required.

## 🛠️ Technologies Used

- **HTML5 & CSS3** (CSS Grid, Flexbox, Keyframe Animations, Backdrop-filters)
- **Vanilla JavaScript** (ES6+)
- **html2canvas** (Client-side PNG rendering)
- **qrcode.js** (Dynamic QR Generation)
- **Lucide-style Inline SVGs** (Modern icons)

## 💡 About The Arrangement Algorithm

The core complexity of this application lies in the `handleAddFlower()` JavaScript function. Rather than horizontal random placement, it utilizes a predefined sequence of tight interlocking angles and drastically dropping "tier-heights" (e.g., `280px -> 215px -> 155px`). 

When a user rapidly clicks to form a bouquet, the logic prevents new front-layer flowers from drowning out the beautiful heads of the older back flowers. The stems dynamically drop downwards exactly 60-70px per layer to perfectly expose the top of the background flowers, creating a truly 3-Dimensional "Handheld Bouquet" dome shape.

## 📝 License

This project is open-source and available under the MIT License.
