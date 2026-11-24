# CLI

We provide a command line interface for training your own NeRFs (no coding necessary). You can learn more about each command by using the `--help` argument.

## Commands

Here are the popular commands that we offer. If you've cloned the repo, you can also look at the [pyproject.toml file](https://github.com/terravision-project/terravision/blob/main/pyproject.toml) at the `[project.scripts]` section for details.

| Command                              | Description                            | Filename                                      |
| ------------------------------------ | -------------------------------------- | --------------------------------------------- |
| [tv-install-cli](ns_install_cli)     | Install tab completion for all scripts | terravision/scripts/completions/install.py     |
| [tv-process-data](ns_process_data)   | Generate a dataset from your own data  | terravision/scripts/process_data.py            |
| [tv-download-data](ns_download_data) | Download existing captures             | terravision/scripts/downloads/download_data.py |
| [tv-train](ns_train)                 | Generate a NeRF                        | terravision/scripts/train.py                   |
| [tv-viewer](ns_viewer)               | View a trained NeRF                    | terravision/scripts/viewer/run_viewer.py       |
| [tv-eval](ns_eval)                   | Run evaluation metrics for your Model  | terravision/scripts/eval.py                    |
| [tv-render](ns_render)               | Render out a video of your NeRF        | terravision/scripts/render.py                  |
| [tv-export](ns_export)               | Export a NeRF into other formats       | terravision/scripts/exporter.py                |

```{toctree}
:maxdepth: 1
:hidden:

ns_install_cli
ns_process_data
ns_download_data
ns_train
ns_render
ns_viewer
ns_export
ns_eval
```
