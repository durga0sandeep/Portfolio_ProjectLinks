# Academic Projects — Durga Sandeep Namballa

M.S. in Computer Science, **DigiPen Institute of Technology** (2026) · Specializing in real-time rendering

This repository collects my graduate course projects in **computer graphics, animation, game engines, machine learning, and deep learning**. Each section below links to the project's own repository.

[Portfolio](https://durga0sandeep.github.io/) 

---

## Contents

- [Computer Graphics & Game Engines](#computer-graphics--game-engines)
  - [Advanced Computer Graphics](#advanced-computer-graphics)
  - [Advanced Real-Time Rendering](#advanced-real-time-rendering)
  - [Advanced Animation and Modeling I](#advanced-animation-and-modeling-i)
  - [Curves and Surfaces](#curves-and-surfaces)
  - [2D Game Engine](#2d-game-engine)
  - [3D Game Engine](#3d-game-engine)
- [Machine Learning & Deep Learning](#machine-learning--deep-learning)
  - [Speech Emotion Recognition](#machine-learning-1--speech-emotion-recognition)
  - [Movie Recommender System](#machine-learning-2--movie-recommender-system)
  - [CNN for Image Classification](#deep-learning--cnn-for-image-classification)
  - [DQN Vacuum Agent](#deep-learning--dqn-vacuum-agent)
- [Tech Stack](#tech-stack)

---

## Computer Graphics & Game Engines

### Advanced Computer Graphics
**C++ · OpenGL · GLSL** · [Repository](#)

A from-scratch 3D rendering pipeline with physically based shading and image-based lighting.

- Core pipeline with homogeneous coordinate transformations and perspective projection
- Physically based microfacet BRDF in GLSL, combining diffuse, specular, and Fresnel terms
- Texture mapping, sky dome rendering, normal mapping, and dual-paraboloid environment reflection mapping
- Two-pass shadow mapping using framebuffer objects (FBOs)
- HDR image-based lighting (IBL) and irradiance mapping

### Advanced Real-Time Rendering
**C++ · OpenGL · GLSL (incl. compute shaders)** · [Repository](#)

A deferred renderer implementing several published real-time rendering techniques.

- **Deferred shading** — multiple-render-target G-buffer; many local lights rendered as additively blended bounding volumes with smooth, range-limited attenuation
- **Shadows** — Moment Shadow Mapping (Peters & Klein, I3D 2015) and Variance Shadow Maps (Donnelly & Lauritzen, I3D 2006) with separable Gaussian blur in compute shaders, plus a comparison of light leaking across methods
- **Variable-size filtering** — replaced the fixed-width blur with summed-area tables (Crow, SIGGRAPH 1984) for constant-time-per-pixel shadow filtering
- **Image-based lighting** — microfacet BRDF with precomputed diffuse irradiance maps (multithreaded CPU integration) and Monte Carlo importance-sampled specular reflection (Colbert & Křivánek, GPU Gems 3), followed by tone mapping and linear-to-sRGB output
- **Ambient occlusion** — Alchemy screen-space ambient obscurance (McGuire et al., HPG 2011) with an edge-aware bilateral filter, applied to ambient lighting only

### Advanced Animation and Modeling I
**C++ · OpenGL** · [Repository](#)

Character animation and physics-based motion for real-time applications.

- Hierarchical character animation with quaternion-based transformations
- Interpolation algorithms and smooth path-following motion
- Forward and inverse kinematics
- Rigid-body dynamics, collision response, and physics-based modeling

### Curves and Surfaces
**JUCE · Unity** · [Repository](#)

An interactive computational geometry application for exploring parametric curves.

- Bézier curves, B-splines, De Casteljau, De Boor, Newton interpolation, and cubic splines
- Real-time curve rendering and visualization
- Interactive editor with dynamic control-point manipulation, knot vector management, and multiple evaluation methods

### 2D Game Engine
**C++ · OpenGL** · 4-member team · [Repository](#)

- Contributed UI systems, debugging tools, and parts of the rendering pipeline for a custom engine
- Developed and evaluated three gameplay prototypes, then shipped the most viable concept as a fully functional game

### 3D Game Engine
**C++ · OpenGL** · 4-member team · Role: Graphics Programmer & Producer · [Repository](#)

- Designed and implemented core engine systems, focusing on rendering and graphics pipeline features
- Built gameplay systems on top of engine capabilities and ran playtests to iterate on performance and user experience

---

## Machine Learning & Deep Learning

### Machine Learning 1 — Speech Emotion Recognition
**Python · NumPy · Seaborn · Matplotlib** · [Repository](#)

- Compared Random Forest and SVM classifiers for 6-class emotion recognition on **CREMA-D (7,442 samples)**
- Macro-AUC of **0.82 (SVM)** vs. **0.80 (Random Forest)** under class imbalance

### Machine Learning 2 — Movie Recommender System
**Python · NumPy · Seaborn · Matplotlib** · Team project · [Repository](#)

- Co-developed a hybrid recommender on **MovieLens 100K**
- Combined K-means++ clustered KNN, SVD matrix factorization, and knowledge-based filtering
- Best RMSE: **1.067**

### Deep Learning — CNN for Image Classification
**TensorFlow/Keras · Google Colab** · [Repository](#)

- Trained CNNs on CIFAR-10, CIFAR-100, and Animal-10, reaching **~78% validation accuracy on CIFAR-10**
- Applied two-phase transfer learning with MobileNetV2
- Config-driven experiment pipeline with checkpointing, TensorBoard logging, early stopping, learning-rate scheduling, and class weighting for class imbalance

### Deep Learning — DQN Vacuum Agent
**PyTorch** · [Repository](#)

- Deep Q-Network built from scratch with experience replay, target networks, and reward shaping
- Scaled training across grid environments from **5×5 to 15×15**

---

## Tech Stack

| Area | Tools |
|---|---|
| Languages | C++, C#, Python, GLSL |
| Graphics | OpenGL, GLFW, GLAD, GLM, Assimp, FreeType, RenderDoc |
| Engines & Frameworks | Unity, JUCE |
| ML / DL | scikit-learn, TensorFlow/Keras, PyTorch, Pandas, NumPy, Matplotlib, Seaborn |
| Tooling | Git, Visual Studio, CMake, Lua, sol2 |
