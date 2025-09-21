# 👷 LLM Engineer's Handbook
<p>
  <a href="https://github.com/pabroux/unvX/blob/master/LICENSE"><img src="https://img.shields.io/github/license/pabroux/llm-engineers-handbook.svg?label=License" alt="License Badge"></a>
  <a href="https://github.com/pre-commit/pre-commit"><img src="https://img.shields.io/badge/pre--commit-enabled-green?logo=pre-commit" alt="pre-commit Badge"></a>
  <a href="https://pixi.sh"><img src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/prefix-dev/pixi/main/assets/badge/v0.json" alt="Pixi Badge"></a>
</p>


This is a [Pixi](https://pixi.sh)-based adaptation of the official repository [LLM Engineer's Handbook](https://github.com/PacktPublishing/LLM-Engineers-Handbook) by [Paul Iusztin](https://github.com/iusztinpaul) and [Maxime Labonne](https://github.com/mlabonne). The primary modification is the replacement of [Poetry](https://github.com/python-poetry/poetry) and its [Poe the Poet](https://github.com/nat-n/poethepoet) plugin with Pixi.

## Table of contents

- [Requirements](#requirements)
- [Install](#install)
- [Usage](#usage)

## Requirements

Compared to the requirements of the official repository, only install the following instead of [Poetry](https://github.com/python-poetry/poetry) and its [Poe the Poet](https://github.com/nat-n/poethepoet) plugin:

- [Pixi](https://pixi.sh)

## Install

All Pixi commands are configured in the `pyproject.toml` file. The `pixi.lock` file records the exact package versions to guarantee reproducibility. These two files are the only ones that differ from the original repository. You can either clone this repository directly or copy just these two files into your clone of the official repository.

Once you have these two files in your repository, install the dependencies as follows:
```shell
pixi install -a
```

## Usage

Replace any call or task made in the book with `poe` by `pixi run`:
```shell
pixi run local-infrastructure-up # is the same as `poe local-infrastructure-up`
```

> [!NOTE]
> Like in the book, I created two other environments:
> - `dev`: related to QA operations.
> - `aws`: related to AWS.
>
> When you work with one of them, call the task by adding the option `-e` followed by the name of the environment. For instance, `poe lint-check` becomes `pixi run -e dev lint-check`.



