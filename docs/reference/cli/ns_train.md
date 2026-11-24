# tv-train

Primary interface for training a NeRF model. `--help` is your friend when navigating command arguments. We also recommend installing the tab completion `tv-install-cli`.

```bash
usage: tv-train {method} [method args] {dataparser} [dataparser args]
```

If you are using a terravision data set, the minimal command is:

```bash
tv-train nerfacto --data YOUR_DATA
```

To learn about the available methods:

```bash
tv-train --help
```

To learn about a methods parameters:

```bash
tv-train {method} --help
```

By default the terravision dataparser is used. If you would like to use a different dataparser it can be specified after all of the method arguments. For a list of dataparser options:

```bash
tv-train {method} {dataparser} --help
```

For example, if you want to specify the `eval_mode` of the terravision dataparser to be `filename` when training your `splatfacto` model via the `tv-train` cli, you can do

```
tv-train splatfacto [method args] terravision-data --eval-mode filename
```

Notice that the custom dataparser and its arguments are passed after specifying the training method and its arguments.
