# example-analysis-package

## introduction
Examples to build WireCell analysis package:

 - `ROOTFrameTap`: is an `IFrameFilter` type of WireCell node.
It reads in `IFrame`s; tap them out to `root` format and output the same `IFrame`s
Analyzers could make `IFrame` analyze nodes by adding analysis code.

## prerequisites
 - Need to have access to a WireCell-Toolkit build.
 - Need to have `root` installed.

## build package

Use `configure /path/to/install` to configure. Modify `configure` as needed.

build and install
```bash
./wcb -p build
./wcb install
```

## run package

Add `<example-analysis-package-lib-location>` to `LD_LIBRARY_PATH`
```bash
path-append <example-analysis-package-lib-location>/lib64 LD_LIBRARY_PATH
```
Run example `jsonnet` configuration in the `cfg` foler
```bash
wire-cell -c wct-sim-check.jsonnet
```

## Other WireCell packages

 - [Simple package](https://github.com/WireCell/example-package)
 - [Zpb](https://github.com/brettviren/wire-cell-zpb)

