# 🎬 Presentation Script: Artist vs. Detective
### *Generative vs. Discriminative Models — Interactive 3D Web Demonstration*

- **Format:** 5-Person Sequential Live Demo
- **Total Duration:** ~10 to 12 minutes (~2 minutes per speaker)
- **Live Demo Site:** [https://xd-arya.github.io/Artist-vs-Detective/](https://xd-arya.github.io/Artist-vs-Detective/)
- **Tech Highlights:** WebGL, Three.js (r128), Client-side Gradient Descent, Interactive 3D Manifolds

---

## 👥 Speaker Roster & Segment Breakdown

| Speaker | Name (Team Role) | Sections Covered | Key Interactive Focus |
| :---: | :--- | :--- | :--- |
| **Speaker 1** | **Arya Pore** | Hero (`#top`), Animal 3D Intuition (`#s-animal`), Dataset Scale-up (`#s-base`) | 3D Hero, Presets, Sliders, Point Clouds |
| **Speaker 2** | **Shanay Puntambekar** | The Dual Philosophy (`#s-idea`), Live Discriminative Demo (`#s-disc`) | 3D Tilt Cards, Real-time Logistic Regression, Testing New Points |
| **Speaker 3** | **Atharva Jaysingpure** | The Generative Manifold (`#s-gen`), Side-by-Side Matrix (`#s-cmp`) | Torus Knot Manifold, Critic Score Drop, Comparison Table |
| **Speaker 4** | **Rishi Gandhi** | Generative Adversarial Networks (`#s-gan`) | Live 3D GAN Particle Stream, Adversarial Dynamics, Mode Collapse |
| **Speaker 5** | **Aditya Divedi** | Team & Wrap-up (`#s-team`), Q&A | Conclusion, Tech Summary, Open Floor |

---

## 🎭 The Complete Presentation Script

---

### 🎙️ SPEAKER 1: The Intuition & Data Representation
**Sections:** `#top` (Hero) $\rightarrow$ `#s-animal` (Animal Explainer) $\rightarrow$ `#s-base` (Scale it up)  
**Target Time:** 0:00 – 2:15 (2 mins 15 secs)

#### 🖥️ Screen Actions:
1. Start at the top of the page. Move your mouse across the hero canvas to demonstrate the 3D interactive particle sphere and rotating partition plane.
2. Slowly scroll to `#s-animal` (**"One animal, three numbers"**).
3. Click the preset button **🐱 Cat A**, then click **🐶 Dog B** to show the values changing.
4. Drag the **Ear pointiness** slider back and forth, then adjust **Snout length** and **Weight**. Notice the gold dot move in 3D space with its pulsing ring.
5. Click and drag the 3D canvas to orbit around the axes (`Ear`, `Snout`, `Weight`).
6. Scroll down to `#s-base` (**"Now scale it up"**) and spin the 200-point red/white cloud.

#### 🗣️ Spoken Script:
> *"Hello everyone! Today our team is thrilled to present **'Artist vs. Detective'** — an interactive 3D exploration of one of machine learning's foundational questions: How do neural networks understand and model data?*
>
> *(Moving cursor across hero)*  
> *When we look at modern AI, models generally do one of two things: they either **tell things apart**, or they **make brand new things**. But before we talk about complex neural networks, let's build the intuition from first principles.*
>
> *(Scrolling to `#s-animal`)*  
> *How does a computer understand an animal? It doesn't see fur or whiskers — it sees numbers. Imagine measuring an animal by three physical traits: **Ear pointiness**, **Snout length**, and **Weight**.*
>
> *(Clicking preset Cat A, then Dog B)*  
> *If we measure Cat A, we get $(9, 3, 4)$. If we measure Dog B, we get $(3, 12, 30)$. Suddenly, these three measurements aren't just a table of numbers — they are **coordinates in 3D space**.*
>
> *(Dragging sliders and rotating the 3D plot)*  
> *As I move these sliders, watch our gold user-dot travel across the coordinate axes. Cats cluster over here because they share sharp ears and low weight. Dogs land on the opposite side with longer snouts and higher mass. Two categories of animals naturally form **two separate clouds of dots**.*
>
> *And this concept generalizes to anything: a house is $(size, bedrooms, age)$; a tiny $28 \times 28$ image is simply a point in 784-dimensional space.*
>
> *(Scrolling to `#s-base` and rotating cloud)*  
> *Now, when we scale up from 4 animals to hundreds of photos, the clouds grow denser, but the geometry remains identical. This brings us to the two fundamental questions in machine learning:*
> 1. *Where is the boundary dividing these two clouds?*
> 2. *What does a cloud actually look like from the inside, so we can place a brand-new point inside it?*
>
> *To explain how the first question is solved, I’ll pass it over to Shanay to introduce the Detective."*

---

### 🎙️ SPEAKER 2: The Core Duality & The Discriminative Detective
**Sections:** `#s-idea` (Two models) $\rightarrow$ `#s-disc` (Discriminative Live Demo)  
**Target Time:** 2:15 – 4:30 (2 mins 15 secs)

#### 🖥️ Screen Actions:
1. Receive presentation control. Scroll down to `#s-idea` (**"Two jobs, two kinds of models"**).
2. Hover over the left card (**"Discriminative: The Detective"**) to trigger the 3D perspective tilt effect.
3. Scroll smoothly into `#s-disc` (**"A discriminative model draws the boundary"**).
4. Point out the initial state: Step `0`, Accuracy `0%`, yellow mistake glows on dots.
5. Click the **Train** button. Watch the yellow glows disappear as the yellow sheet tilts and aligns between the red and white points, and accuracy climbs above 90%.
6. Click **Test a new point**. Observe the gold test dot appear and read the classification result.
7. Click **Test a new point** 2-3 more times to show both Cat and Dog classifications with confidence scores.

#### 🗣️ Spoken Script:
> *"Thank you, Arya!*
>
> *(Hovering over the Detective card)*  
> *This brings us to our first persona: **The Detective**, formally known as a **Discriminative Model**. Mathematically, it learns the conditional probability $P(Y \mid X)$ — given this data point, which class does it belong to?*
>
> *Crucially, the Detective doesn't care what a cat or dog looks like in general. It only cares about where the **boundary** between them sits. If you give it a picture, it acts like a courtroom judge: 'Is this a cat or a dog?'*
>
> *(Scrolling to `#s-disc`)*  
> *To prove how this works, we built a live, client-side **Logistic Regression classifier with Gradient Descent** right inside this WebGL canvas. Nothing here is pre-computed or video.*
>
> *(Pointing to canvas at step 0)*  
> *Initially, our decision hyperplane — this yellow flat sheet — starts in a completely random position. It slices right through both groups. Notice the yellow halos around several dots: those are misclassified animals.*
>
> *(Clicking 'Train')*  
> *Now watch what happens when I hit **Train**! With every training step, gradient descent computes the classification error and tilts the sheet. The yellow error glows fade away, and our accuracy climbs past 90%. The sheet has successfully found the optimal gap separating cats from dogs.*
>
> *(Clicking 'Test a new point')*  
> *Now let's test it on unseen data. When I click **'Test a new point'**, a new gold dot drops into the space. The model inspects which side of the sheet it falls on and immediately outputs its prediction — for example, '94% Cat' or '88% Dog'.*
>
> *This is how real-world spam filters, face recognition, and medical diagnostics work: draw the boundary, and check which side new data lands on.*
>
> *But what if we don't want to sort existing photos? What if we want to create one from scratch? For that, Atharva will introduce our Artist."*

---

### 🎙️ SPEAKER 3: The Generative Artist & Manifold Learning
**Sections:** `#s-gen` (Generative live demo) $\rightarrow$ `#s-cmp` (Side-by-side comparison)  
**Target Time:** 4:30 – 6:45 (2 mins 15 secs)

#### 🖥️ Screen Actions:
1. Receive presentation control. Scroll to `#s-gen` (**"A generative model learns what real data looks like"**).
2. Click and rotate the 3D scene to show the **white knot manifold** and the scattered **gold noise points**.
3. Point out the critic metric: `Step 0`, `Critic catches fakes: 98%`.
4. Click **Train generator**. Watch the gold dots smoothly flow and lock onto the surface of the white knot.
5. Highlight the critic score falling from **98% down toward ~50%**.
6. Click **Generate new samples** to show a fresh burst of points finding the manifold.
7. Scroll down to `#s-cmp` (**"Side by side"**) and highlight the comparative rows.

#### 🗣️ Spoken Script:
> *"Thank you, Shanay!*
>
> *(Showing the 3D knot scene in `#s-gen`)*  
> *Now let’s look at the other side of machine learning: **The Artist**, or the **Generative Model**. Instead of learning a dividing line, generative models learn the distribution of the data itself — modeling $P(X)$.*
>
> *In reality, genuine photos don't scatter randomly throughout space; they live on a complex, lower-dimensional structure called a **data manifold**. Here, we represent that real data distribution as this intricate **white 3D torus knot**.*
>
> *(Pointing to the scattered gold dots)*  
> *Generative models don't start with finished art — they start with **random noise**, represented by these scattered gold dots. The pipeline is: **Noise $\rightarrow$ Generator $\rightarrow$ Synthetic Sample**.*
>
> *(Clicking 'Train generator')*  
> *Watch closely as I press **Train generator**. The network learns the mapping, and the scattered noise particles migrate directly onto the white manifold. Once they land on the manifold, they become authentic-looking new examples.*
>
> *(Pointing to the Critic readout)*  
> *Notice this crucial metric: **'Critic catches fakes'**. At step zero, when the dots were scattered chaos, the critic caught fakes 98% of the time. But as our generator masters the shape of the manifold, the critic's score drops to 50%.*
>
> *Why is a falling score good? Because 50% is a coin flip! When the detective can only guess at random, the generator has created fakes so convincing they are indistinguishable from reality.*
>
> *(Clicking 'Generate new samples')*  
> *Every time we inject fresh noise, we produce brand-new points on the knot — just like Midjourney or ChatGPT generating endless unique variations.*
>
> *(Scrolling to `#s-cmp`)*  
> *Summarizing side-by-side: The Detective answers 'Which group is this?' and outputs a label; the Artist answers 'What would a new one look like?' and outputs synthetic data.*
>
> *Now, what happens when you combine the Detective and the Artist into one single system? Rishi will show you the power of GANs."*

---

### 🎙️ SPEAKER 4: The Ultimate Synergy — GANs
**Sections:** `#s-gan` (Better together: The GAN)  
**Target Time:** 6:45 – 8:45 (2 mins)

#### 🖥️ Screen Actions:
1. Receive presentation control. Scroll to `#s-gan` (**"Better together: the GAN"**).
2. Rotate the wide 3D interactive GAN scene: show the **Artist (left generator)** streaming particles toward the **Detective (right red discriminator gate)**.
3. Click the **Pause / Resume** button to freeze a frame of particles passing through the decision barrier, and point to the fool percentage: `Fakes that fool the detective: ~X%`.
4. Point out the 4 informational cards below the demo (The game, Why it works, Where it is used, Watch out / Mode collapse).
5. Scroll down to highlight the concluding banner:  
   *`Discriminative models decide. Generative models create.`*
6. Hand off to Aditya for the final wrap-up.

#### 🗣️ Spoken Script:
> *"Thank you, Atharva!*
>
> *(Interacting with `#s-gan` canvas)*  
> *In 2014, Ian Goodfellow and his team asked a brilliant question: What if we take the Detective and the Artist and make them play a game against each other? That is the origin of the **Generative Adversarial Network**, or **GAN**.*
>
> *Here on screen, you see this rivalry in action:*
> - *On the left, we have the **Generator (The Artist)**, continuously producing candidate samples from random seeds.*
> - *On the right, we have the **Discriminator (The Detective)**, acting as a red checkpoint filter.*
>
> *(Highlighting the particle stream and pausing)*  
> *Every time the Detective catches an artifact or flaw, the Artist adjusts its parameters to avoid that mistake in the future. As the Artist improves, the Detective must sharpen its discrimination skills. This game pushes both models to superhuman fidelity.*
>
> *(Referencing the four cards)*  
> *GANs revolutionized image enhancement, super-resolution, and deepfake synthesis. However, they are notoriously delicate to train — prone to phenomena like **mode collapse**, where the generator gets lazy and produces the exact same output repeatedly. That’s why modern image architectures increasingly rely on diffusion models.*
>
> *(Scrolling to the concluding quote)*  
> *To summarize the core message of our project in six words:*  
> **'Discriminative models decide. Generative models create.'**
>
> *On that note, I'll pass over to Aditya for our final reflections and to take your questions."*

---

### 🎙️ SPEAKER 5: Conclusion, Tech & Wrap-up
**Sections:** `#s-team` (The team behind it), Q&A  
**Target Time:** 8:45 – 10:30 (1 min 45 secs)

#### 🖥️ Screen Actions:
1. Receive presentation control. Scroll into `#s-team` (**"The team behind it"**) to show all five member cards.
2. Briefly navigate back to the hero (`#top`) using the nav bar to give the audience a final sweeping look of the whole page from top to bottom.
3. Keep the hero canvas visible with mouse parallax active during Q&A.

#### 🗣️ Spoken Script:
> *"Thank you, Rishi!*
>
> *(Scrolling to `#s-team`)*  
> *Let me introduce everyone who contributed to this project: Arya Pore, Shanay Puntambekar, Atharva Jaysingpure, Rishi Gandhi, and myself, Aditya Divedi.*
>
> *What you've seen today is a fully client-side, zero-framework web application built on vanilla WebGL and Three.js r128 — with real gradient descent, real manifold generation, and a real adversarial game all running directly in your browser. No server, no pre-recorded video, no shortcuts.*
>
> *The site is live and accessible to anyone at:*  
> **[https://xd-arya.github.io/Artist-vs-Detective/](https://xd-arya.github.io/Artist-vs-Detective/)**
>
> *(Clicking the 'Try it' nav link to scroll back to `#s-animal`)*  
> *We encourage you to drag the sliders, click Train, and experiment — because the best way to understand these models is to play with them.*
>
> *Thank you for your attention. We are now happy to take any questions."*

---

## 💡 Practical Rehearsal & Live Demo Tips

1. **Screen Resolution & Zoom:** Keep browser zoom at `100%` or `90%` so the 3D canvases have ample breathing room.
2. **Smooth Scrolling:** Use trackpad or mouse wheel smoothly — the site has built-in **Lenis smooth-scrolling** which creates fluid cinematic transitions between sections.
3. **Orbiting 3D Views:** Whenever a speaker mentions 3D coordinates, point clouds, or planes, give the canvas a gentle drag. The built-in inertial rotation adds instant professional polish.
4. **Verbal Handoffs:** Practice the 5-second handoff sentences between each speaker — crisp transitions make the team look tightly coordinated.
5. **Emergency Reset:** If you want to re-demonstrate the Logistic Regression or Generative demo during Q&A, every demo panel includes a clean **Reset** button.
