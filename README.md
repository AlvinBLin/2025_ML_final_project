This is the place where I'll upload the process of my final project to the course machine learning taken in 2025 fall, opened by Te-Sheng Lin.

Adaptive Traffic Control with Physics-Informed Reinforcement Learning

## Overview

This project explores a novel approach to mitigating urban traffic congestion, specifically addressing the "ghost green light" phenomenon common in high-density areas like Hsinchu City. By integrating the physical laws of traffic flow (Lighthill-Whitham-Richards model) with decentralized decision-making (Max Pressure), we demonstrate a scalable and robust alternative to traditional fixed-time signal control.

## Motivation: Solving the "Ghost Green Light"

In many cities, commuters often face red lights on jammed arterial roads while intersecting streets—despite being empty—hold a green light. This project aims to eliminate such inefficiencies by developing an intelligent control agent that dynamically allocates green time based on real-time demand and queue pressure.

## Methodology

Structural Model: A $N \times N$ "Tian" grid network, inspired by the high-density Eixample district of Barcelona, Spain, serves as a rigorous testbed for urban gridlock.

Physics Engine: Traffic flow is simulated using the Cell Transmission Model (CTM), a discrete implementation of fluid dynamic conservation laws, ensuring realistic queue propagation and spillback behavior.

Control Strategy: A decentralized Max Pressure agent operates at each intersection, making greedy, local decisions to equalize queue lengths without needing computationally expensive global optimization.

## Key Findings

Our scalability analysis reveals that while fixed-time controllers fail as network complexity grows ($N \ge 6$), the Max Pressure agent maintains robust performance. In large-scale grids ($20 \times 20$), the adaptive system consistently reduces average waiting times by over 11%, saving thousands of vehicle-hours and effectively preventing network-wide gridlock.

---

# Run the AI Studio app

<img width="1384" height="511" alt="image" src="https://github.com/user-attachments/assets/8e8d2863-69e3-4dae-bd50-5fa31d3f830e" />

View the visualisation of training process on my AI Studio: https://ai.studio/apps/drive/1J_4vOOTEAZkYQG8lp9GSj7z-5Aa-dRSW

## Run Locally

**Prerequisites:**  Node.js

1. Install dependencies:
   `npm install`
2. Set the `GEMINI_API_KEY` in [.env.local](.env.local) to your Gemini API key
3. Run the app:
   `npm run dev`

