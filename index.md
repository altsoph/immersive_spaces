This page contains supplementary demos for our paper "[Unrolling Virtual Worlds for Immersive Experiences](#)" accepted for [NeurIPS 2023 Workshop on Machine Learning for Creativity and Design](https://nips.cc/virtual/2023/workshop/66545).
We explore the idea of generation of navigable 3D worlds using the combination of modern neural networks and specific geometric transformations to achieve interactive, locally coherent worlds.

First, we utilize the fine-tuned [StableDiffusion v1.5 model](https://huggingface.co/runwayml/stable-diffusion-v1-5) to generate panoramas in equirectangular projection, similar to [BlockadeLabs](https://www.blockadelabs.com/) and [latentlabs360](https://civitai.com/models/10753/latentlabs360).
We then process the projection by applying 3D transformation to generate an image corresponding to the projection from another point in the same space. Finally, after obtaining the distorted projection, we "heal" this distortion by running the image through the model again, using a technique similar to the "in-painting." The network tends to "reconstruct" inputs, thereby enhancing their likelihood, grounding various noisy or distorted objects onto this manifold and projecting them to the nearest suitable region (read more details in the [paper](#)). By repetition of these three steps, we are able to construct interactive, locally coherent worlds with graphs of available locations, similar to the legendary [Myst](https://en.wikipedia.org/wiki/Myst) game or Google Street View interface. To render these interactive spaces, we use an open-source library called [Pannellum](https://pannellum.org/).

## Interactive Demo Spaces

  * [*a maze of twisty little passages, all alike*](zork/index.html)
  * [*a dark, mysterious cave filled with bright, glowing green crystals and large, looming statues*](crystals/index.html)
  * [*an outdoor desert landscape, with large sand dunes and jagged rocks*](desert/index.html)  

## Some screencasts

<img src="https://github.com/altsoph/immersive_spaces/blob/main/imgs/_000607_o3.gif?raw=true" alt="twisted passages, all alike" /> <img src="https://github.com/altsoph/immersive_spaces/blob/main/imgs/_221253_o3.gif?raw=true" alt="emerald cave with golems" /> <img src="https://github.com/altsoph/immersive_spaces/blob/main/imgs/_221414_o3.gif?raw=true" alt="hedgehog in the fog" /> <img src="https://github.com/altsoph/immersive_spaces/blob/main/imgs/_223927_o3.gif?raw=true" alt="night city maze" /> <img src="https://github.com/altsoph/immersive_spaces/blob/main/imgs/_224117_o3.gif?raw=true" alt="server room maze" /> <img src="https://github.com/altsoph/immersive_spaces/blob/main/imgs/_224256_o3.gif?raw=true" alt="magic mushroom forest" />

&copy;&nbsp;[altsoph](https://altsoph.com), 2023