# TerraVision

**A toolkit for creating, training, and exploring neural radiance fields (NeRFs).**

TerraVision provides a modular workflow for preparing image and video captures, training neural rendering models, viewing results, and exporting geometry.

> **Project origin:** TerraVision is a modified derivative of [Nerfstudio](https://github.com/nerfstudio-project/nerfstudio), based on its 1.1.5 release. It is not affiliated with or endorsed by the original authors. The upstream project is licensed under [Apache-2.0](https://github.com/nerfstudio-project/nerfstudio/blob/v1.1.5/LICENSE); retain applicable copyright and attribution notices when redistributing this code.

## Features

- Train NeRF models, including Nerfacto and vanilla NeRF.
- Process images, video, and supported capture formats into training datasets.
- Inspect training runs in the web viewer and create camera paths.
- Render videos and export point clouds.
- Configure and extend data parsers, models, and pipelines.

## Requirements

Training is designed for an NVIDIA GPU with CUDA. Linux is recommended; Windows support is less tested. See the [installation guide](docs/quickstart/installation.md) for supported Python, PyTorch, CUDA, and build-tool requirements.

## Install from source

```bash
git clone https://github.com/Pradeep-Kumar-30/Terravision.git
cd Terravision
python -m pip install --upgrade pip setuptools
python -m pip install -e .
```

For development tools and platform-specific setup, follow the [installation guide](docs/quickstart/installation.md).

## Quickstart: train a model

Download the sample capture and train Nerfacto:

```bash
tv-download-data terravision --capture-name=poster
tv-train nerfacto --data data/terravision/poster
```

The training command prints a viewer URL when the viewer is enabled. To see the available models and options:

```bash
tv-train --help
tv-train nerfacto --help
```

More examples are in [Training your first model](docs/quickstart/first_nerf.md).

## Use your own data

Prepare image, video, or supported capture data with `tv-process-data`, then train on the resulting dataset:

```bash
tv-process-data images --data /path/to/images --output-dir /path/to/processed
tv-train nerfacto --data /path/to/processed
```

See the [custom dataset guide](docs/quickstart/custom_dataset.md) for COLMAP setup and format-specific instructions.

## View, render, and export

Open an existing training run in the viewer:

```bash
tv-viewer --load-config /path/to/config.yml
```

Use the viewer's camera-path controls to create a render command, or inspect command options directly:

```bash
tv-render --help
tv-export pointcloud --help
```

## Documentation

- [Installation](docs/quickstart/installation.md)
- [First model](docs/quickstart/first_nerf.md)
- [Custom datasets](docs/quickstart/custom_dataset.md)
- [Existing datasets](docs/quickstart/existing_dataset.md)
- [Export geometry](docs/quickstart/export_geometry.md)
- [Developer guides](docs/developer_guides/)
- [API reference](docs/reference/api/)

## Citation

TerraVision is derived from Nerfstudio. If you use the underlying framework in research, cite the original work:

```bibtex
@inproceedings{tancik2023nerfstudio,
  title     = {Nerfstudio: A Modular Framework for Neural Radiance Field Development},
  author    = {Tancik, Matthew and Weber, Ethan and Ng, Evonne and Li, Ruilong and Yi, Brent and Kerr, Justin and Wang, Terrance and Kristoffersen, Alexander and Austin, Jake and Salahi, Kamyar and Ahuja, Abhik and McAllister, David and Kanazawa, Angjoo},
  booktitle = {ACM SIGGRAPH 2023 Conference Proceedings},
  year      = {2023}
}
```

## License and acknowledgments

This derivative follows the upstream Apache-2.0 license; see the [upstream license text](https://github.com/nerfstudio-project/nerfstudio/blob/v1.1.5/LICENSE). It builds on Nerfstudio and its contributors, as well as libraries including [Tyro](https://github.com/brentyi/tyro) and [nerfacc](https://github.com/nerfstudio-project/nerfacc). Please consult their respective licenses and preserve applicable notices. Add the applicable license file to this repository before redistributing it.
