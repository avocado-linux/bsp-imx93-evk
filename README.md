# bsp-imx93-evk

Board support for the i.MX 93 EVK

## Using this extension

`bsp-imx93-evk` is an [Avocado](https://avocadolinux.org) extension — a reusable fragment of
build- and runtime-configuration that you compose into your own Avocado project. To use it,
declare it as a package-sourced extension in your `avocado.yaml` and add it to a runtime:

```yaml
extensions:
  avocado-bsp-imx93-evk:
    source:
      type: package
      version: "*"        # or pin an exact version

runtimes:
  my-runtime:
    extensions:
      - avocado-bsp-imx93-evk
```

Then `avocado build`. The extension's config is fetched from your target's package feed
and merged into your project at build time.
