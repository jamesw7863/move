# MOVE

**MOVE** is a real-time computer vision movement game built with Next.js and MediaPipe Pose. The game uses a player’s webcam to track body movement, detect poses, and control gameplay through physical motion instead of a keyboard or controller.

MOVE was built during **ShellHacks 2025** as an interactive fitness-inspired web game combining computer vision, browser-based performance, and responsive game logic.

## Overview

MOVE turns a webcam into a motion controller. Players move their body to avoid hazards, trigger actions, and score points in a fast-paced 3x3 grid game. The project explores how pose estimation can make web games more active, accessible, and engaging.

The system uses real-time pose tracking to detect player position and movement, then translates that data into game interactions with low-latency feedback.

## Features

* Real-time body tracking using **MediaPipe Pose**
* Webcam-based motion controls
* 3x3 hazard-dodging game layout
* Collision detection and scoring system
* Pause behavior when the player leaves the camera frame
* Persistent high-score storage
* Responsive UI for different screen sizes
* Browser-based gameplay with no external hardware required

## Tech Stack

* **Framework:** Next.js
* **Language:** TypeScript
* **Styling:** Tailwind CSS
* **Computer Vision:** MediaPipe Pose
* **Machine Learning:** TensorFlow
* **Graphics/Performance:** WebGPU, WebGL
* **Deployment:** Vercel

## How It Works

1. **Webcam input**

   * The app accesses the user’s webcam through the browser.

2. **Pose detection**

   * MediaPipe Pose estimates body landmarks in real time.

3. **Movement mapping**

   * Player position is mapped onto a 3x3 game grid.

4. **Game logic**

   * The app checks for collisions, updates score, and manages game state.

5. **Frame handling**

   * If the player leaves the camera frame, the game pauses to prevent unfair collisions.

6. **Score tracking**

   * High scores are saved locally so players can track their best runs.

## Performance Goals

MOVE was designed to support smooth real-time interaction directly in the browser.

* Tracks player movement at up to **60 FPS**
* Maintains low-latency input response under approximately **80ms**
* Tested by **40+ users** during ShellHacks 2025

## Getting Started

This section is for developers who want to run the project locally.

### Prerequisites

Make sure you have the following installed:

```bash
Node.js
npm
```

### Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
```

Navigate into the project directory:

```bash
cd YOUR_REPOSITORY_NAME
```

Install dependencies:

```bash
npm install
```

Run the development server:

```bash
npm run dev
```

Open the app in your browser:

```bash
http://localhost:3000
```

## Project Structure

```bash
app/
  page.tsx
  layout.tsx

components/
  # Game UI and reusable interface components

lib/
  # Utility functions and game logic

public/
  # Static assets
```

## Future Improvements

* Add multiple difficulty levels
* Add multiplayer or challenge modes
* Improve calibration for different camera angles
* Add more detailed motion analytics
* Add sound effects and animations
* Add leaderboard support
* Improve accessibility for different mobility ranges

## Inspiration

MOVE was inspired by the idea that games can encourage physical activity while still being lightweight and accessible through a normal browser. Instead of requiring a console, controller, or VR headset, MOVE uses computer vision to make movement-based gameplay available with only a webcam.

## Author

Built by Diego Oberto, Devon Trenoskie, Hector Cordero, and James Williams during ShellHacks 2025.
