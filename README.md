# example-analysis-package

## introduction
Examples to build WireCell analysis package.

### `ExampleROOTAna`
`ExampleROOTAna` is an `IFrameFilter` type of WireCell node.
It reads in `IFrame`s; tap them out to `root` format and output the same `IFrame`s
Analyzers could perform analysis on the `IFrame`s and modify the `root` output as needed.

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


