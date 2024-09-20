Real-Time Game Simulation Using Diffusion Models

Author: [Wendi Fan](https://www.linkedin.com/in/wendi-fan-265996310/) (**ORCID: 0000-0003-0284-9166**)

📌 The article introduces GameNGen, a pioneering game engine powered entirely by a neural model. It showcases the ability to simulate interactive environments, such as the classic game DOOM, in real-time at high quality, operating at over 20 frames per second (FPS) on a TPU.

Article link: https://arxiv.org/abs/2408.14837

🔹 Traditional game engines are manually coded to process user inputs, update the game state, and render graphics. This study explores a shift to neural models to automate the game simulation process, raising the question of whether neural networks can simulate complex games like DOOM in real-time while maintaining high visual quality.

🔹 GameNGen stands as the first demonstration of a real-time interactive game engine fully powered by diffusion models, utilizing an augmented version of Stable Diffusion v1.4. The study contributes significant innovations, including the use of a reinforcement learning (RL) agent to gather game data and a diffusion model to predict future frames. The real-time frame prediction and game state persistence over long trajectories mark a breakthrough in interactive game simulation.

🔹 The model successfully simulates DOOM at 20 FPS with a visual quality comparable to the original game. Human evaluators found it difficult to distinguish between the simulated game and the original in short clips. The study demonstrates that noise augmentation mitigates auto-regressive drift, preserving image quality over long sequences. However, cross-domain simulations (other games) remain a challenge.

🔹 While GameNGen represents a step toward a new paradigm of AI-driven game engines, further improvements in model architecture and memory access are required for broader applications. Future work might include experimenting with more complex games and improving the RL agent's ability to explore various game scenarios.

📑 Valevski, D., Leviathan, Y., Arar, M., Fruchter S. (2024).  Diffusion models are real-time game engines. DOI: 10.48550/arXiv.2408.14837.