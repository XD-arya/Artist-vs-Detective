# 🎨 Artist vs. 🕵️ Detective: Generative vs Discriminative Models

> **"Telling things apart versus Making new ones."**  
> An interactive, 3D educational web application that brings core machine learning concepts to life directly in your browser using Three.js and WebGL.

[![Live Demo](https://img.shields.io/badge/Demo-Live_on_GitHub_Pages-2ea44f?style=for-the-badge&logo=githubpages)](https://xd-arya.github.io/Artist-vs-Detective/)
[![Three.js](https://img.shields.io/badge/Three.js-r128-black?style=for-the-badge&logo=three.js)](https://threejs.org/)
[![WebGL](https://img.shields.io/badge/WebGL-Interactive_3D-990000?style=for-the-badge&logo=webgl)](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](#license)

---

## 🌐 Live Demo

Experience the full interactive 3D website live at:  
👉 **[https://xd-arya.github.io/Artist-vs-Detective/](https://xd-arya.github.io/Artist-vs-Detective/)**

---

## 📖 The Core Idea

Machine learning models fundamentally approach data from one of two perspectives:

| Paradigm | Persona | Mathematical Objective | Core Question |
| :--- | :--- | :--- | :--- |
| **Discriminative** | 🕵️ **The Detective** | Models $P(\text{label} \mid \text{data})$ | *"Is this photo a cat or a dog?"* |
| **Generative** | 🎨 **The Artist** | Models $P(\text{data})$ | *"Show me a cat that never existed."* |

This project provides an intuition-first visual journey where high-dimensional abstract concepts are projected into interactive 3D spaces with algorithms running live in your browser.

---

## 🌟 Interactive Experience & Features

```
┌────────────────────────────────────────────────────────────────────────┐
│                        Interactive Journey                             │
├─────────────────┬───────────────────┬──────────────────┬───────────────┤
│ 1. 3D Intuition │ 2. Dataset Scale  │ 3. Classification│ 4. Generation │
│  (Animal Point) │  (Point Clouds)   │ (Logistic Reg.)  │  (3D Manifold)│
└─────────────────┴───────────────────┴──────────────────┴───────────────┘
```

### 1. 🐾 One Animal, Three Numbers (`#s-animal`)
- **Intuition**: Demystifies how continuous physical entities become coordinates in space.
- An animal is described by three measurable traits:
  - **Ear pointiness** ($0 - 10$)
  - **Snout length** ($0 - 15\text{ cm}$)
  - **Weight** ($1 - 40\text{ kg}$)
- **Interactive Controls**:
  - Quick presets: **Cat A**, **Cat B**, **Dog A**, **Dog B**.
  - Dynamic sliders with live coordinate badges `(x, y, z)`.
  - Live 3D scatter plot with labeled coordinate axes, preset clusters, and a glowing gold user marker with a pulsing ring.
- **Dimensionality Analogy**: Connects the 3D toy example to houses $(size, bedrooms, age)$ and real-world images ($28 \times 28\text{ grayscale} = 784\text{ dimensions}$).

### 2. 📈 Now Scale It Up (`#s-base`)
- Scales the 4-animal mental model into a real dataset of hundreds of photo points.
- Illustrates how high-dimensional feature vectors naturally group into labeled clouds.
- Frames the two core problems in machine learning:
  1. *Where is the boundary between clouds?* $\rightarrow$ **Discriminative**
  2. *What does a cloud look like so we can draw a new one?* $\rightarrow$ **Generative**

### 3. ⚖️ Two Jobs, Two Kinds of Models (`#s-idea` & `#s-cmp`)
- Interactive 3D perspective tilt cards:
  - **Discriminative (The Detective)**: Focuses strictly on the decision boundary. Simple, fast, and accurate for classification.
  - **Generative (The Artist)**: Learns how the data is distributed in space. Capable of synthesis and creative generation.
- Full side-by-side comparison matrix covering outputs, real-world examples, and trade-offs.

### 4. 🎯 Live In-Browser Classification Demo (`#s-disc`)
- **Real-Time Client-Side ML**: Runs actual **Logistic Regression with Gradient Descent** live inside WebGL — no static recordings or mockups.
- **Dynamic Decision Surface**: Watch the 3D separating hyperplane sheet dynamically tilt and rotate to separate cats from dogs as accuracy climbs.
- **Test a New Point**: Inject unseen test points and watch the trained model classify them on the fly with live confidence readouts.

### 5. ✨ Live In-Browser Generative Demo (`#s-gen`)
- **Manifold Learning**: Demonstrates how generative models transform arbitrary random noise into structured samples mapped to a 3D manifold (torus knot).
- **Critic Feedback**: Tracks the discriminator's detection score as synthetic samples gradually become indistinguishable from real data.

### 6. ⚔️ Better Together: The GAN (`#s-gan`)
- Explains the min-max adversarial rivalry (Goodfellow et al., 2014).
- Particle stream visualization showing generated gold points attempting to pass through the detective's red gate.
- Explains real-world applications (style transfer, super-resolution) and pitfalls (mode collapse).

---

## 🛠️ Tech Stack & Architecture

- **Single-File Architecture**: Clean, standalone [`index.html`](file:///a:/College/DRL/index.html) with zero build steps or bundlers required.
- **3D Graphics Engine**: [Three.js](https://threejs.org/) (r128) WebGL canvas rendering:
  - Custom procedural point clouds & particle materials.
  - Interactive orbit controls, ray-casted drags, and directional lighting.
  - Dynamic mathematical mesh generation (planes, spheres, torus knots).
- **Typography & Styling**:
  - [Bricolage Grotesque](https://fonts.google.com/specimen/Bricolage+Grotesque) typography.
  - CSS custom properties design system with responsive layouts and glassmorphic panels.
  - 3D interactive pointer-tilt cards.
- **Animation & Physics**:
  - [Lenis](https://github.com/darkroomengineering/lenis) smooth inertial scrolling.
  - Custom `IntersectionObserver` scroll-reveal hooks.

---

## 🚀 Local Development

To run the project locally on your machine:

### Option 1: Direct File Open
Double-click [`index.html`](file:///a:/College/DRL/index.html) or open it directly in any modern browser (Chrome, Firefox, Safari, Edge).

### Option 2: Local HTTP Server (Recommended)
```bash
# Using Python 3
python -m http.server 8000

# Using Node / npx
npx serve .
```
Then navigate to `http://localhost:8000`.

---

## 👥 The Team

Built by:

| Avatar | Name | Roll / ID |
| :---: | :--- | :---: |
| 🔴 **AP** | **Arya Pore** | `33267` |
| 🟡 **SP** | **Shanay Puntambekar** | `33273` |
| 🔴 **AJ** | **Atharva Jaysingpure** | `33237` |
| 🟡 **RG** | **Rishi Gandhi** | `33226` |
| 🔴 **AD** | **Aditya Divedi** | `33201` |

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).