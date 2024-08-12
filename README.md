# PyVista tutorials

> This tutorial was co-authored by [xieliaokc](https://github.com/xieliaokc) and [liaoweiyang2017](https://github.com/liaoweiyang2017). If you have any questions, please contact [liaoweiyang2013@outlook.com](mailto:liaoweiyang2013@outlook.com).
>
> 本教程是由[xieliaokc](https://github.com/xieliaokc)和[liaoweiyang2017](https://github.com/liaoweiyang2017)共同撰写，如果你有任何疑问请联系[liaoweiyang2013@outlook.com]([mailto:liaoweiyang2013@outlook.com])。

## Installation

> We recommend using `Anaconda` to manage your Python environment, and `Mamba` for faster package installation. The commands below are based on `Anaconda` and `Mamba`.

- First, download the `Mambaforge` package from the [Mamba download page](https://github.com/conda-forge/miniforge#mambaforge). Choose the version that matches your system. `Mambaforge` is a minimal conda distribution that includes both `Mamba` and `conda`. After downloading, install it with:

  ```bash
  bash Miniforge3-Linux-x86_64.sh -b -p ${HOME}/mambaforge
  ```

- Next, add `Mamba` and `conda` to your `PATH` by editing your `~/.bashrc` file. Add the following lines to the end of the file:

  ```bash
  vim ~/.bashrc
  
  # conda
  if [ -f "${HOME}/mambaforge/etc/profile.d/conda.sh" ]; then
      source "${HOME}/mambaforge/etc/profile.d/conda.sh"
  fi
  # mamba
  if [ -f "${HOME}/mambaforge/etc/profile.d/mamba.sh" ]; then
      source "${HOME}/mambaforge/etc/profile.d/mamba.sh"
  fi
  ```

- You can alias the `conda` command to `mamba` for convenience. Add this line to your `~/.bashrc` file:

  ```bash
  vim ~/.bashrc
  
  alias conda=mamba
  ```

- Now, create the `pyvista` environment with the following commands:

  ```bash
  # create the pyvista environment using Python version 3.9
  mamba create -n pyvista python=3.9
  mamba activate pyvista
  
  # install packages
  pip install matplotlib numpy
  pip install pyvista jupyter notebook
  
  # install Google Drive support for downloading provided datasets
  pip install gdown
  ```

- We recommend using `vscode` to run `.ipynb` notebook files. You can open the `ipynb` files directly with `vscode`.

## Purpose of This Tutorial

1. **Enhancing the Use of Scripting for 3D Visualization**: This tutorial aims to assist users in better utilizing scripts to create 3D volumes and various slices. This method is more efficient and repeatable compared to traditional manual operations, especially for complex visualization requirements.
2. **Offering a Free and Precise Alternative**: In contrast to commercial software like `Voxler` or `ParaView`, which often require manual adjustments and lack precision, this tutorial uses `PyVista` to provide a free, open-source solution that allows users to precisely control the visualization process.
3. **Emphasizing the Spirit of Open Source and Sharing**: The tutorial embraces the spirit of open-source and sharing, intending to help more people gain proficiency in professional tools and to promote the dissemination and exchange of technical knowledge.

---

## 安装说明

> 我们推荐使用 `Anaconda` 来管理 Python 环境，并使用 `Mamba` 来加速软件包的安装。以下命令基于 `Anaconda` 和 `Mamba`。

- 首先，从 [Mamba 下载页面](https://github.com/conda-forge/miniforge#mambaforge) 下载 `Mambaforge` 包。请选择与你的系统匹配的版本。`Mambaforge` 是一个包含 `Mamba` 和 `conda` 的简化 conda 发行版。下载后，可以用以下命令安装：

  ```bash
  bash Miniforge3-Linux-x86_64.sh -b -p ${HOME}/mambaforge
  ```

- 接下来，通过编辑 `~/.bashrc` 文件，将 `Mamba` 和 `conda` 添加到你的 `PATH`。在文件末尾添加以下行：

  ```bash
  vim ~/.bashrc
  
  # conda
  if [ -f "${HOME}/mambaforge/etc/profile.d/conda.sh" ]; then
      source "${HOME}/mambaforge/etc/profile.d/conda.sh"
  fi
  # mamba
  if [ -f "${HOME}/mambaforge/etc/profile.d/mamba.sh" ]; then
      source "${HOME}/mambaforge/etc/profile.d/mamba.sh"
  fi
  ```

- 为方便起见，可以将 `conda` 命令别名为 `mamba`。在 `~/.bashrc` 文件中添加这一行：

  ```bash
  vim ~/.bashrc
  
  alias conda=mamba
  ```

- 现在，可以使用以下命令创建 `pyvista` 环境：

  ```bash
  # 使用 Python 版本 3.9 创建 pyvista 环境
  mamba create -n pyvista python=3.9
  mamba activate pyvista
  
  # 安装软件包
  pip install matplotlib numpy
  pip install pyvista jupyter notebook
  
  # 安装 Google Drive 支持以下载提供的数据集
  pip install gdown
  ```

- 我们建议使用 `vscode` 来运行 `.ipynb` 笔记本文件。你可以直接用 `vscode` 打开 `ipynb` 文件。

## 写这个教程的原因

1. **促进三维绘图脚本的应用**：本教程旨在帮助大家更好地使用脚本来绘制三维体图和各种切片。这种方法较传统手动操作更高效和可重复，适合更批量化等复杂的可视化需求。
2. **提供免费、精准的替代方案**：相比商业付费软件如 `Voxler` 或 `ParaView`，这些软件常需要手动调节且不够精准，本教程将通过 `PyVista` 提供一个免费的开源解决方案，使用户能够精确控制可视化过程。
3. **支持开源共享精神**：本教程秉持开源共享的精神，希望帮助更多人掌握专业工具，并促进技术知识的传播和交流。

---
