# NeRFPlayer

<h4>A Streamable Dynamic Scene Representation with Decomposed Neural Radiance Fields</h4>


```{button-link} https://lsongx.github.io/projects/nerfplayer.html
:color: primary
:outline:
Paper Website
```

```{button-link} https://github.com/lsongx/nerfplayer-terravision
:color: primary
:outline:
TerraVision add-on code
```

[![NeRFPlayer Video](https://img.youtube.com/vi/flVqSLZWBMI/0.jpg)](https://www.youtube.com/watch?v=flVqSLZWBMI)


## Installation

First install terravision dependencies. Then run:

```bash
pip install git+https://github.com/lsongx/nerfplayer-terravision.git
```

## Running NeRFPlayer

Details for running NeRFPlayer can be found [here](https://github.com/lsongx/nerfplayer-terravision). Once installed, run:

```bash
tv-train nerfplayer-ngp --help
```

Two variants of NeRFPlayer are provided:

| Method                | Description                                     |
| --------------------- | ----------------------------------------------- |
| `nerfplayer-nerfacto` | NeRFPlayer with nerfacto backbone               |
| `nerfplayer-ngp`      | NeRFPlayer with instant-ngp-bounded backbone    |


## Method Overview

![method overview](https://lsongx.github.io/projects/images/nerfplayer-framework.png)<br>
First, we propose to decompose the 4D spatiotemporal space according to temporal characteristics. Points in the 4D space are associated with probabilities of belonging to three categories: static, deforming, and new areas. Each area is represented and regularized by a separate neural field. Second, we propose a hybrid representations based feature streaming scheme for efficiently modeling the neural fields.

Please see [TODO lists](https://github.com/lsongx/nerfplayer-terravision#known-todos) to see the unimplemented components in the terravision based version.