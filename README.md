About doclang-feedstock
=======================

Feedstock license: [BSD-3-Clause](https://github.com/conda-forge/doclang-feedstock/blob/main/LICENSE.txt)

Home: https://www.doclang.ai/

Package license: Apache-2.0

Summary: DocLang reference toolkit

Documentation: https://github.com/doclang-project/doclang/blob/main/README.md

<p align="center">
  <a href="https://github.com/doclang-project/doclang">
    <img loading="lazy" alt="DocLang" src="https://github.com/doclang-project/doclang/raw/main/resources/logo.png" width="30%"/>
  </a>
</p>

# DocLang

[![PyPI version](https://img.shields.io/pypi/v/doclang)](https://pypi.org/project/doclang/)
![Python](https://img.shields.io/badge/python-3.10%20%7C%20%203.11%20%7C%203.12%20%7C%203.13%20%7C%203.14-blue)
[![uv](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/uv/main/assets/badge/v0.json)](https://github.com/astral-sh/uv)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
[![Checked with mypy](https://www.mypy-lang.org/static/mypy_badge.svg)](https://mypy-lang.org/)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![License Apache 2.0](https://img.shields.io/github/license/doclang-project/doclang)](https://opensource.org/licenses/Apache-2.0)

**[DocLang](https://www.doclang.ai/) is the AI-native markup format for unstructured content** — including documents, images, and more. It maps cleanly to LLM tokens while preserving structure, semantics, layout, and geometry in a single, unambiguous representation.

This repository is the home of the normative specification and the reference toolkit for DocLang. If you build with LLMs and VLMs on real-world content, this is where the standard lives.

## Specification

The source of the specification is available in [spec.md](https://github.com/doclang-project/doclang/blob/main/spec.md)
and exports to different formats can be found in the [exports/](https://github.com/doclang-project/doclang/tree/main/exports)
directory.

## Reference Toolkit

The commands below illustrate basic scenarios. For advanced installation and usage options
(minimal install, platform notes, custom Schematron backends, Python API), see the
[toolkit README](https://github.com/doclang-project/doclang/blob/main/doclang/README.md).

### Installation

```bash
pip install "doclang[schematron-saxon]"
```

### Validation

```bash
doclang validate -n my_document.dclg
```

### Packaging

```bash
doclang pack my_document.dclg
```

## Citation

If you use DocLang in academic or technical work, please cite the specification:

```bibtex
@misc{doclang_2026,
  title        = {DocLang: Universal AI Document Format},
  author       = {{DocLang Project}},
  year         = {2026},
  version      = {main},
  howpublished = {\url{https://github.com/doclang-project/doclang}},
}
```

## Development

To work on this repository — setup, tests, reference generation, releases — see [CONTRIBUTING.md](https://github.com/doclang-project/doclang/blob/main/CONTRIBUTING.md).

## We ❤️ Open Source AI

DocLang is developed in the open and supported by the [LF AI & Data Foundation](https://lfaidata.foundation/projects/). Learn more about the project at [doclang-project](https://github.com/doclang-project).

## License

DocLang is licensed under the Apache License 2.0. See [LICENSE](https://github.com/doclang-project/doclang/blob/main/LICENSE) for details.

Current build status
====================


<table><tr>
    <td>All platforms:</td>
    <td>
      <a href="https://github.com/conda-forge/doclang-feedstock/actions/workflows/conda-build.yml">
        <img src="https://github.com/conda-forge/doclang-feedstock/actions/workflows/conda-build.yml/badge.svg?event=push&branch=main">
      </a>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-doclang-green.svg)](https://anaconda.org/conda-forge/doclang) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/doclang.svg)](https://anaconda.org/conda-forge/doclang) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/doclang.svg)](https://anaconda.org/conda-forge/doclang) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/doclang.svg)](https://anaconda.org/conda-forge/doclang) |

Installing doclang
==================

Installing `doclang` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
conda config --set channel_priority strict
```

Once the `conda-forge` channel has been enabled, `doclang` can be installed with `conda`:

```
conda install doclang
```

or with `mamba`:

```
mamba install doclang
```

It is possible to list all of the versions of `doclang` available on your platform with `conda`:

```
conda search doclang --channel conda-forge
```

or with `mamba`:

```
mamba search doclang --channel conda-forge
```

Alternatively, `mamba repoquery` may provide more information:

```
# Search all versions available on your platform:
mamba repoquery search doclang --channel conda-forge

# List packages depending on `doclang`:
mamba repoquery whoneeds doclang --channel conda-forge

# List dependencies of `doclang`:
mamba repoquery depends doclang --channel conda-forge
```


About conda-forge
=================

[![Powered by
NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](https://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[Azure](https://azure.microsoft.com/en-us/services/devops/), [GitHub](https://github.com/),
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/),
[Drone](https://cloud.drone.io/welcome), and [TravisCI](https://travis-ci.com/)
it is possible to build and upload installable packages to the
[conda-forge](https://anaconda.org/conda-forge) [anaconda.org](https://anaconda.org/)
channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance,
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information, please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating doclang-feedstock
==========================

If you would like to improve the doclang recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/doclang-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks, and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@kklein](https://github.com/kklein/)

