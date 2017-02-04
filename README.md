![studiomdl][studiomdl_banner]

## Overview

studiomdl compiles [Studio Model Data][SMD] from [QC files][QC] to a [model file][MDL].

This is a cross-platform compatible version of [studiomdl][studiomdl_wiki] for Half-Life (GoldSrc).

## Prerequestites

- `gcc` or `clang`

## Installing & Building

Clone this project.

```sh
git clone https://github.com/fnky/studiomdl.git
cd studiomdl
```

```sh
make
make install # optional
```

You can set architecture (default `-m32`), compiler (default `gcc`) and install path (default `/usr/local/bin`) as well as user flags for custom C flags.


```sh
make CC=clang ARCH=-m64 INSTALL_PATH=/usr/bin USER_FLAGS="-O3 -march=native"
```

> **Note:** 64-bit build currently doesn't work, due to structs not using compatible data types.

## Usage

```sh
studiomdl [options] <QC file>
```

#### Options

<dl>
  <dt><code>-t</code></dt>
  <dd>texture</dd>

  <dt><code>-r</code></dt>
  <dd>tag reversed</dd>

  <dt><code>-n</code></dt>
  <dd>tag bad normals</dd>

  <dt><code>-f</code></dt>
  <dd>flip all triangles</dd>

  <dt><code>-a</code></dt>
  <dd>normal blend angle</dd>

  <dt><code>-h</code></dt>
  <dd>dump hboxes</dd>

  <dt><code>-i</code></dt>
  <dd>ignore warnings</dd>

  <dt><code>-g size</code></dt>
  <dd>max sequencegroup size</dd>
</dl>

> Note: Your QC and SMD files has to use `LF` (Unix) line-endings in order to work.

## Contribute

See the [guidelines for contributing][].

## License

[Half Life 1 SDK LICENSE](LICENSE)

[SMD]: https://developer.valvesoftware.com/wiki/Studio_Model_Data
[QC]: https://developer.valvesoftware.com/wiki/QC
[MDL]: https://developer.valvesoftware.com/wiki/Model
[studiomdl_wiki]: https://developer.valvesoftware.com/wiki/Studiomdl
[guidelines for contributing]: https://github.com/fnky/studiomdl/blob/master/CONTRIBUTING.md
[studiomdl_banner]: https://raw.githubusercontent.com/fnky/studiomdl/master/img/banner.png
