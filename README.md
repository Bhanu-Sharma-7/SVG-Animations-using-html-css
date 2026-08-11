# 🎨 SVG Animations using HTML & CSS

A collection of sleek, lightweight, dynamic **SVG Animations** built natively using **HTML5**, **CSS3**, and **SVG SMIL**. This repository demonstrates various key techniques for animating vector graphics on the web, including line-drawing effects, motion paths, property pulsing, and animated text path tracking.

---

## ✨ Features & Animation Techniques

This repository showcases **4 distinct SVG animation techniques**:

1. ✒️ **Signature Line-Drawing Animation**
   - **Technique:** CSS `@keyframes` using `stroke-dasharray` and `stroke-dashoffset` combined with SVG `pathLength="1"`.
   - **Effect:** Smooth self-drawing stroke animation mimicking hand-drawn signatures or line art.

2. ⚽ **Motion Path Traversal (`offset-path`)**
   - **Technique:** CSS `offset-path` property and `offset-distance`.
   - **Effect:** An element (a circle) glides seamlessly along a custom Bezier curve SVG path.

3. 💓 **Pulsing SVG Circle (SMIL Animation)**
   - **Technique:** Native SVG `<animate>` tag targeting the radius (`r`) attribute.
   - **Effect:** Smooth pulsing / heartbeat effect created declaratively inside SVG without external JS or CSS.

4. 🌊 **Wave Text Along Path**
   - **Technique:** SVG `<textPath>` combined with SMIL `<animate>` targeting `startOffset`.
   - **Effect:** Dynamic text scrolling smoothly along a curved vector line.

---

## 🛠️ Tech Stack

- **HTML5** – Modern semantic markup & inline SVG graphics
- **CSS3** – `@keyframes`, `offset-path`, and stroke dashboard animation techniques
- **SVG & SMIL** – Native Declarative Vector Graphics Animation

---

## 📂 Project Structure

```
SVG Animation/
├── index.html     # Page structure containing SVG elements and SMIL animations
├── style.css      # Global styling, layout, CSS keyframes, and motion path logic
└── README.md      # Project documentation
```

---

## 🚀 Getting Started

No build step, compilers, or external dependencies required!

### Quick Run
1. **Clone the repository:**
   ```bash
   git clone https://github.com/Bhanu-Sharma-7/SVG-Animations-using-html-css.git
   ```
2. **Navigate to the project folder:**
   ```bash
   cd SVG-Animations-using-html-css
   ```
3. **Open `index.html`** directly in any modern browser (Chrome, Firefox, Edge, Safari).

---

## 💡 Code Highlights & How It Works

### 1. Self-Drawing Stroke (CSS + SVG)
```html
<path class="signature" pathLength="1" d="M10,80 C60,10 120,120 180,40 S260,10 290,60" fill="none" stroke="#fff" stroke-width="4" />
```
```css
.signature {
    stroke-dasharray: 1;
    stroke-dashoffset: 1;
    animation: svg-path-animation 1s linear infinite alternate;
}

@keyframes svg-path-animation {
    to {
        stroke-dashoffset: 0;
    }
}
```

### 2. Following an SVG Path (`offset-path`)
```css
.ball {
    offset-path: path('M10,120 C120,-20 280,320 390,30');
    animation: along-path 3s linear infinite alternate;
}

@keyframes along-path {
    from { offset-distance: 0%; }
    to { offset-distance: 100%; }
}
```

### 3. Declarative SVG Pulsing (SMIL)
```html
<circle cx="60" cy="60" r="15">
  <animate
    attributeName="r"
    values="15;30;15"
    dur="2s"
    repeatCount="indefinite"
  />
</circle>
```

---

## 👤 Author

**Bhanu Sharma**
- GitHub: [@Bhanu-Sharma-7](https://github.com/Bhanu-Sharma-7)

---

## 📜 License

This repository is open-source and free to use under the [MIT License](LICENSE).
