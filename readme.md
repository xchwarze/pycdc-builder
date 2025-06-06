# Decompyle++ Build Pipeline for Indetectables Toolkit

This repository provides an automated build and release process for [Decompyle++](https://github.com/zrax/pycdc), a Python bytecode disassembler and decompiler.

It is used to build the tool and publish precompiled binaries as part of the [Indetectables Toolkit](https://github.com/indetectables-net/toolkit).

## Overview

- The repository runs a GitHub Actions pipeline to:
  - Clone the official Decompyle++ source
  - Build it automatically
  - Package the `pycdc` and `pycdas` binaries
  - Publish them as a GitHub Release with a unique tag (`YYYYMMDD-SHORTSHA`)
- The [Universal Updater](https://github.com/xchwarze/universal-tool-updater) fetches the latest release and integrates the binaries into the toolkit.

## Output

The pipeline produces:

```

release/
├── pycdc
└── pycdas

```

These files are consumed by the toolkit under:

```

toolkit/Decompilers/[PYTHON] Python Decompyle++/

```

## Upstream

Decompyle++ is maintained at:
> https://github.com/zrax/pycdc

All credit to the original authors. This repository does not modify or maintain the tool itself — it only builds and packages it.

## License

The binaries are distributed under the terms of the GNU General Public License v3, as per the upstream project.

---
Maintained by the [Indetectables Team](https://github.com/indetectables-net)

