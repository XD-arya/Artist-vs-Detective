# 🧠 Generative vs Discriminative Models: 3D Interactive Explainer

> **"Telling things apart versus Making new ones."**  
> An interactive, 3D educational web experience that brings core machine learning concepts to life directly in your browser using Three.js and WebGL.

[![Three.js](https://img.shields.io/badge/Three.js-r128-black?style=flat&logo=three.js)](https://threejs.org/)
[![WebGL](https://img.shields.io/badge/WebGL-Interactive_3D-990000?style=flat&logo=webgl)](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API)
[![Status](https://img.shields.io/badge/Status-Complete-success?style=flat)](#)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](#license)

---

## 📖 Overview

Machine learning models are often divided into two philosophical and mathematical categories:
- **Discriminative models** (*The Detective*): Learn decision boundaries between classes to answer *"Which category does this example belong to?"* — modeling $P(Y \mid X)$.
- **Generative models** (*The Artist*): Learn the underlying probability distribution of the data to answer *"What would a new, realistic sample look like?"* — modeling $P(X)$ or $P(X, Y)$.

This project delivers an intuition-first interactive guide and visual sandbox where abstract high-dimensional concepts are mapped to intuitive 3D coordinate spaces with live training algorithms executing client-side in real time.

---

## 🌟 Interactive Modules & Features

```
┌────────────────────────────────────────────────────────────────────────┐
│                        Interactive Journey                             │
├─────────────────┬───────────────────┬──────────────────┬───────────────┤
│ 1. 3D Intuition │ 2. Dataset Scale  │ 3. Classification│ 4. Generation │
│  (Animal Point) │  (Point Clouds)   │ (Logistic Reg.)  │  (3D Manifold)│
└─────────────────┴───────────────────┴──────────────────┴───────────────┘
```

### 1. 🐾 One Animal, Three Numbers (`#s-animal`)
- **Core Intuition**: Demystifies how real-world entities become data points. An animal is described by three measurable traits:
  - **Ear pointiness** ($0 - 10$)
  - **Snout length** ($0 - 15\text{ cm}$)
  - **Weight** ($1 - 40\text{ kg}$)
- **Interactive Controls**:
  - Quick presets: **Cat A**, **Cat B**, **Dog A**, **Dog B**.
  - Dynamic sliders updating coordinates $(x, y, z)$ in real time.
  - Live 3D scatter plot featuring labeled coordinate axes, preset animal spheres, and a glowing gold user marker with an animated pulse ring.
- **Dimensionality Analogy**: Extends the intuition to houses $(size, bedrooms, age)$ and digital images ($28 \times 28 \text{ grayscale} = 784\text{ dimensions}$).

### 2. 📈 Dataset Scaling (`#s-base`)
- Smoothly scales the 4-animal mental model into a full dataset containing hundreds of examples.
- Explains the emergence of **feature clusters** and presents the two guiding questions of machine learning:
  1. *Where is the boundary between the clouds?* $\rightarrow$ **Discriminative**
  2. *What does a cloud look like so we can draw a new one?* $\rightarrow$ **Generative**

### 3. ⚖️ The Detective vs. The Artist (`#s-idea` & `#s-cmp`)
- 3D interactive tilt cards illustrating model philosophies:
  - **Discriminative**: Focuses strictly on the boundary. Fast, efficient, answers *"Is this a cat or dog?"*
  - **Generative**: Understands the entire data distribution. Generates novel samples, answers *"Show me a cat that never existed."*
- Side-by-side comparison table covering mathematical definitions, real-world examples, and trade-offs.

### 4. 🎯 Live Discriminative Training Demo (`#s-disc`)
- **Real-Time Client-Side Learning**: Runs actual **Logistic Regression with Gradient Descent** live inside WebGL — no fake animations or pre-recorded video.
- **Visual Hyperplane**: Watch the 3D separating sheet dynamically pivot and slide into the optimal decision boundary as accuracy climbs.
- **Interactive Testing**: Drop brand-new random test points into the space to observe real-time classification inferences with confidence ratings.

### 5. ✨ Live Generative Manifold Demo (`#s-gen`)
- **Distribution Modeling**: Demonstrates how generative models convert raw random noise vectors into structured data samples lying on a complex 3D manifold (torus knot).
- **Adversarial Critic Scoring**: Demonstrates how a critic/discriminator score evolves as generated samples become indistinguishable from the training distribution.

### 6. ⚔️ Generative Adversarial Networks (`#s-gan`)
- Interactive visualization of the adversarial min-max game (Goodfellow et al., 2014).
- Dynamic particles streaming from the Generator through the Discriminator gate, tracking fool rate percentages and explaining failure modes like mode collapse.

---

## 🛠️ Tech Stack & Architecture

- **Zero-Build Architecture**: Entire web application is contained within a clean, dependency-free [`index.html`](file:///a:/College/DRL/index.html) file.
- **3D Graphics**: [Three.js](https://threejs.org/) (r128) WebGL rendering engine with custom shaders, procedural particle systems, dynamic meshes, and canvas textures.
- **Kinetic Typography & Design**: Styled with modern typography ([Bricolage Grotesque](https://fonts.google.com/specimen/Bricolage+Grotesque)), CSS custom properties, glassmorphism, and responsive CSS grid.
- **Smooth Navigation**: [Lenis](https://github.com/darkroomengineering/lenis) for inertial scroll physics combined with custom `IntersectionObserver` triggers for entry animations.

---

## 🚀 Getting Started

No `npm install`, build step, or bundler required.

### Option 1: Direct Browser Launch
Simply double-click or open [`index.html`](file:///a:/College/DRL/index.html) directly in any modern web browser (Chrome, Firefox, Safari, Edge).

### Option 2: Local HTTP Server (Recommended)
Running through an HTTP server ensures full asset loading and smooth WebGL context initialization:

```bash
# Using Python 3
python -m http.server 8000

# Using Node / npx
npx serve .
```
Then navigate to `http://localhost:8000` in your browser.

---

## 📚 Course Materials & Repository Contents

This repository is part of coursework in **Deep Learning and Reinforcement Learning (DRL)**:

| File | Description |
| :--- | :--- |
| [`index.html`](file:///a:/College/DRL/index.html) | Interactive 3D web application: Generative vs Discriminative Models |
| `1. Module - I - Intro to Deep Learning.pptx` | Lecture slides on Deep Learning fundamentals and neural architectures |
| `2. Module - I - Intro to Reinforcement Learning.pptx` | Lecture slides on MDPs, value iteration, policy iteration, and RL basics |
| `3. Module - I - Deep_Reinforcement_Learning.pptx` | Lecture slides on Deep Q-Networks (DQN), Policy Gradients, and Actor-Critic |
| `Question Bank Module I ... .docx` | Comprehensive review questions for Module I |
| `Asn3.pdf`, `Asn4.pdf`, `Asn5.pdf` | Course assignments and problem sets |

---

## 👥 Authors & Team

Created by:

| Avatar | Name | Roll / ID |
| :---: | :--- | :---: |
| 🔴 **AP** | **Arya Pore** | `33267` |
| 🟡 **SP** | **Shanay Puntambekar** | `33273` |
| 🔴 **AJ** | **Atharva Jaysingpure** | `33237` |
| 🟡 **RG** | **Rishi Gandhi** | `33226` |

---

## 📄 License

This project is licensed under the MIT License — feel free to explore, learn from, and adapt the code for educational and research purposes.