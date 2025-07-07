# 👷 LLM Engineer's Handbook
<p>
  <a href="https://github.com/pabroux/unvX/blob/master/LICENSE">
    <picture>
      <img src="https://img.shields.io/github/license/pabroux/unvX.svg?label=Licence" alt="License Badge">
    </picture>
  </a>
  <a href="https://pixi.sh">
    <picture>
      <img src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/prefix-dev/pixi/main/assets/badge/v0.json" alt="pixi Badge">
    </picture>
  </a>
</p>


This is a [pixi](https://pixi.sh)-based adaptation of the official repository [LLM Engineer's Handbook](https://github.com/PacktPublishing/LLM-Engineers-Handbook) by [Paul Iusztin](https://github.com/iusztinpaul) and [Maxime Labonne](https://github.com/mlabonne). The primary modification is the replacement of [poetry](https://github.com/python-poetry/poetry) and its [poe the poet](https://github.com/nat-n/poethepoet) plugin with pixi.

## Table of contents

- [Requirements](#requirements)
- [Install](#install)
- [Usage](#usage)

## Requirements

Compared to the requirements of the official repository, only install the following instead of [poetry](https://github.com/python-poetry/poetry) and its [poe the poet](https://github.com/nat-n/poethepoet) plugin:

- [pixi](https://pixi.sh)

## Install

All pixi commands are configured in the `pyproject.toml` file. The `pixi.lock` file records the exact package versions to guarantee reproducibility. These two files are the only ones that differ from the original repository. You can either clone this repository directly or copy just these two files into your clone of the official repository.

## Usage

First, install the dependencies:
```shell
pixi install -a
```

Then, replace any call or task made in the book with `poe` by `pixi run`:
```shell
pixi run local-infrastructure-up # is the same as `poe local-infrastructure-up`
```

> [!NOTE]
> Like in the book, I created two other environments:
> - `dev`: related to QA operations.
> - `aws`: related to AWS.
>
> When you work with one of them, call the task by adding the option `-e` followed by the name of the environment. For instance, `poe lint-check` becomes `pixi run -e dev lint-check`.



