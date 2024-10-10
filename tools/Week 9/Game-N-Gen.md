# GameNGen

_The Future of Real-Time Game Simulation_


![Gamengen Logo](https://i.imgur.com/AMBO9ID.png)
<div  align="center"><i>Google's GameNGen</i></div>


## Author

* Aditya Iyengar (ORCID: [0009-0005-1959-9724](https://orcid.org/0009-0005-1959-9724))

## Introduction

In recent years, artificial intelligence (AI) has made astounding strides in transforming industries from healthcare to creative arts. Now, the gaming industry is poised for a revolution thanks to **GameNGen**—a pioneering project from Google Research and Tel Aviv University. GameNGen represents a breakthrough in the use of **diffusion models** for real-time game simulation, enabling interactive environments that respond to user input with an unprecedented level of fidelity. Unlike traditional game engines, which rely heavily on code-based systems to manage assets and game logic, GameNGen is driven entirely by a neural network that predicts the next game frame based on previous ones. 

In this article, we will explore the intricate details of GameNGen, its potential impact on the gaming industry, and the technology that powers it. From the diffusion model at its core to its reinforcement learning-based training methodology, this deep dive into GameNGen will cover every key aspect of this groundbreaking tool.

## What is GameNGen?

**GameNGen** (pronounced "game engine") is an AI-powered game engine that generates game environments and interactive sequences in real time using a neural model. It is built using a **diffusion model**, which is a class of generative AI that excels at predicting subsequent visual outputs based on prior inputs. In this case, GameNGen uses gameplay frames and player actions to predict the next frame in the sequence, rendering it without the need for traditional game engine coding techniques.

The diffusion model was originally based on **Stable Diffusion 1.4**, a widely used image-generation model. However, Google’s research team modified this model to condition frame generation on previous game states and user actions, enabling a real-time, interactive experience. GameNGen’s ability to simulate gameplay, particularly for the 1993 cult classic **DOOM**, has made headlines across the tech industry.

![gameplay](https://i.imgur.com/gY5AV9q.png)
<div  align="center"><i>gameplay screenshot of AI-generated DOOM using GameNGen from arXiv:2408.14837</i></div>


## The Technology Behind GameNGen

### Diffusion Models and Frame Prediction

The core of GameNGen lies in the use of **diffusion models**. These models typically work by introducing noise to an image and then learning how to reverse the noise over several steps, thereby recovering the original image. In GameNGen’s case, the diffusion model predicts the next frame in a game based on the player’s actions and the previous frame. The model generates high-fidelity graphics in real time, updating each frame as the player moves through the game.

Training this model involves recording gameplay sessions where an **RL-agent** (reinforcement learning agent) interacts with the game environment. The RL-agent’s actions, observations, and game states are collected to form a vast dataset. This dataset is used to train the diffusion model to predict the next frame in real time while preserving the interactive and dynamic nature of the game.

![RL Training](https://i.imgur.com/hlrSWD9.png)
<div  align="center"><i>RL-agent training visual from TechTalks</i></div>


### Reinforcement Learning and Data Collection

One of the most critical components of GameNGen is its use of **reinforcement learning (RL)** for data generation. A specialized RL-agent was trained to play *DOOM*, gathering approximately **900 million frames** during gameplay. The agent was trained using a teacher-forcing objective, ensuring that it could mimic diverse playing styles and create a varied dataset. 

Instead of being optimized to achieve high scores, the RL-agent was designed to interact with the environment in a way that is representative of human gameplay. This approach ensures that the training data captures typical in-game actions, such as shooting enemies, navigating levels, and interacting with items. The RL-agent recorded its own observations, health levels, and other in-game variables, which were then used to guide the neural model in simulating similar game sequences.

### Training the Diffusion Model

GameNGen was trained using a **pre-trained checkpoint from Stable Diffusion 1.4**. All U-Net parameters were unfrozen to allow the model to fine-tune itself for generating gameplay frames. The training process utilized a **batch size of 128**, a learning rate of **2e-5**, and the **Adafactor optimizer** without weight decay. A maximum noise level of **0.7** was used to introduce variability in frame generation, ensuring that the model could recover from inconsistencies and maintain visual fidelity during gameplay. 

![architecture](https://i.imgur.com/9lgAWAf.png)
<div  align="center"><i>GameNGen architecture diagram from arXiv:2408.14837</i></div>


The model was trained over 700,000 steps using **128 TPU v5e accelerators**, generating approximately 900 million frames. The large-scale training infrastructure allowed GameNGen to achieve **real-time performance at 20 frames per second (fps)** on a single TPU. While this performance is lower than the 60 fps typical of modern gaming, it is an impressive feat for a neural model operating without a traditional game engine.

![TPU v5e](https://i.imgur.com/0JH4mir.png)
<div  align="center"><i>TPU v5e architecture from google cloud docs</i></div>


## GameNGen’s Performance and Real-Time Simulation

The standout feature of GameNGen is its **real-time performance**. During inference, GameNGen is capable of generating **over 20 fps** at a visual quality comparable to the original *DOOM*. Human evaluators, when shown side-by-side comparisons between gameplay clips generated by GameNGen and those rendered by the original *DOOM* engine, had difficulty distinguishing between the two. In short, the AI-generated gameplay is nearly indistinguishable from the real game, at least for short clips.

One key challenge tackled by the developers was ensuring **frame stability** during long sequences. Initially, the model suffered from degradation in image quality as time progressed, which was mitigated by augmenting the training process with **noise-based regularization**. This allowed GameNGen to maintain a stable image quality over longer gameplay sessions.

However, one limitation of the model is its **memory window**. The AI can only "remember" about **three seconds of gameplay** at a time, meaning it has limited capacity to handle long-term dependencies or complex strategies. Despite this, it manages to recreate most in-game states (like ammo and health counters) accurately over the short-term window.

![doomgamengen](https://i.imgur.com/rWtpG9k.png)
<div  align="center"><i>AI-generated Doom Gameplay by heise online</i></div>


![original-doom](https://i.imgur.com/8gjpV8W.jpeg)
<div  align="center"><i>Original 1993 Doom Gameplay by TrueAchievements</i></div>

## Applications and Future Potential

#### Beyond DOOM: Expanding to Other Games

While GameNGen has been primarily demonstrated with *DOOM*, its underlying architecture could theoretically be applied to any video game. With additional training, the model could generate entirely new games, or even create **custom modifications (mods)** for existing titles based on user inputs. For instance, GameNGen could create a new level or character using nothing more than a series of example images or a few gameplay frames.

The potential here extends beyond merely replicating classic games. **Procedural generation**—creating new content dynamically—could allow for entirely new genres of gaming, where the game world evolves in real-time based on player actions. Developers might one day use GameNGen to craft games without needing to write millions of lines of code.

#### Implications for Game Development

By shifting game creation from a code-based to an AI-based process, GameNGen could revolutionize the gaming industry. Currently, game development is labor-intensive and expensive, with large teams required to create assets, write game logic, and debug code. GameNGen’s generative nature could allow small teams—or even individuals—to develop sophisticated games with much fewer resources.

There is also the potential for **interactive storytelling**. Since GameNGen can respond to user actions in real time, it might eventually be used to create immersive, evolving narratives that adapt to the player's choices, further blurring the line between creator and consumer.


### Limitations and Challenges

Despite its revolutionary potential, GameNGen does face several limitations:

1. **Performance Constraints**: While 20 fps is a significant achievement for an AI-based engine, modern games typically require at least 60 fps for smooth gameplay. For now, GameNGen is limited to simpler, older games like *DOOM*.
   
2. **Memory and Long-Term Dependencies**: With only a three-second memory window, GameNGen struggles with long-term gameplay elements, such as remembering strategies or handling complex scenarios that unfold over time.
   
3. **Training Costs**: Training GameNGen requires a massive computational infrastructure, including hundreds of TPUs and millions of dollars in hardware costs. This may limit its accessibility to larger organizations with deep pockets.

4. **Generalization**: GameNGen’s current version is optimized for specific games like *DOOM*. While it shows promise for other games, each new game would require extensive retraining, a process that is both time-consuming and expensive.

## Conclusion

**GameNGen** is a revolutionary tool that pushes the boundaries of what’s possible with AI in gaming. While it is still in its early stages and has some limitations, it opens up a new realm of possibilities for real-time interactive game environments powered by neural networks. As the technology continues to evolve, we may see a future where games are no longer coded but rather generated on-the-fly by AI, fundamentally transforming the way we experience digital worlds.


This deep dive into GameNGen shows that while we are still in the early days of AI-generated games, the future is bright. With further research and development, this tool could dramatically reduce the time and cost associated with game development and open up new creative avenues for designers, developers, and players alike.

## References

- BD TechTalks (2021). _Reinforcement learning improves game testing, EA’s AI team finds_. Available at: [https://bdtechtalks.com/2021/10/04/ea-reinforcement-learning-game-testing/](https://bdtechtalks.com/2021/10/04/ea-reinforcement-learning-game-testing/).

- Valevski, D., Leviathan, Y., Arar, M., & Fruchter, S. (2024). _GameNGen: Diffusion models are real-time game engines_. Available at: [https://arxiv.org/pdf/2408.14837](https://arxiv.org/pdf/2408.14837).

- Google Cloud (n.d.). _TPU v5e documentation_. Available at: [https://cloud.google.com/tpu/docs/v5e](https://cloud.google.com/tpu/docs/v5e).

- Heise Online (2024). _GameNGen: Google researchers simulate Doom without an engine_. Available at: [https://www.heise.de/en/news/GameNGen-Google-researchers-simulate-Doom-without-an-engine-9851171.html](https://www.heise.de/en/news/GameNGen-Google-researchers-simulate-Doom-without-an-engine-9851171.html).

- TrueAchievements (n.d.). _DOOM (1993) screenshots_. Available at: [https://www.trueachievements.com/game/DOOM-1993/screenshots](https://www.trueachievements.com/game/DOOM-1993/screenshots).