# Lab 1: Introduction to Simulation and Data Analysis

![MIT License](https://img.shields.io/github/license/BEE4850/lab01?style=for-the-badge)

This is the repository for Lab 1 for [BEE 4850](https://viveks.me/simulation-data-analysis), taught at [Cornell University](https://cornell.edu) in Spring 2024 by [Vivek Srikrishnan](https://viveks.me).

If enrolled in the class, a PDF of the completed notebook, **with all cells evaluated**, should be submitted to Gradescope *no later* than Friday, February 2, 2024, at 9:00pm. 10% will be deducted for each day that the notebook is late.

## Learning Objectives

After completing this lab, students will be able to:

- write functions in Julia;
- simulate alternative datasets to test a hypothesis;
- make plots to compare summaries of observed datasets to alternatives.


## Repository Overview

The repository consists of the following files:

- `lab01.ipynb`: Jupyter Notebook for the homework assignment. Students should create code or Markdown blocks as necessary to answer questions. **This is the only file you should need to edit.**
- `Project.toml`, `Manifest.toml`: Julia environment files. These should just work, but feel free to add other packages as needed using the `Pkg` package manager. **This is the only other file that you might end up making changes to, though you should do this using `Pkg`, not directly.**
- `lab01.qmd`: Source file for Jupyter notebook generation. You shouldn't need to or want to touch this; everything is in the `.ipynb` file.
- `LICENSE`: This material is licensed using the MIT license. You can ignore this for working on the problem set.
- `README.md`: This file. You shouldn't need to touch this.
- `.gitignore`: This tells `git` what files to ignore. You shouldn't need to touch this.
- `.github/`: This folder contains workflow files which generate the notebook. Again, you shouldn't need to touch this.

## Dependencies

This lab uses on the following packages:

- `Random.jl`
- `StatsBase.jl`
- `Plots.jl`

## Prerequisites

1. [Install Julia](https://julialang.org/downloads/) before beginning this lab. This notebook was developed with version 1.8.3, but any 1.8.x should work (there could be some issues with other versions, depending on what's changed).
2. If necessary, [install git](https://happygitwithr.com/install-git.html) and [create a GitHub account](https://github.com). 
3. [Clone the repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository). I recommend doing this in a dedicated `BEE4850/` folder, which can also house homework assignment repositories and lecture notes. You can clone directly into the `BEE4850/` folder.   For Windows (or from another graphical interface), just create a `BEE4850` folder, then a `labs` folder inside of that, then clone into that folder. Or to clone into a `BEE4850/labs` folder, from a command prompt:
    ```bash
    cd BEE4850/
    mkdir labs
    cd labs/
    git clone https://github.com/BEE4850/lab01.git
    ```

## Opening The Notebook

1. To interact (view and run) the notebook, there are two options:
  - Install an integrated development environment, or IDE (I recommend [VS Code](https://code.visualstudio.com/) with the [Julia extension](https://marketplace.visualstudio.com/items?itemName=julialang.language-julia)). 
  - Use the [`IJulia.jl` package](https://github.com/JuliaLang/IJulia.jl). I've included this in the project environment (discussed below), so no further steps are needed.  
2. Opening the notebook will depend on what you decided to do in the previous step. 
  - If you installed VS Code, you should be able to just open `lab01.ipynb` and everything should just work. 
  - If you're using a different IDE, Google how to make sure that it is set up to run a Julia notebook.
  - If you want to use `IJulia.jl`, open a Julia prompt. You can do this by:
    - Using the `Julia-1.8` or equivalent graphical program, type `cd("BEE4850/labs")` or whatever path points to your lab notebook folder;
    - Navigating to your `BEE4850/labs/lab01` folder and typing `julia` to open the prompt.Then:
    
      ```julia
      import Pkg
      Pkg.activate(".")
      using IJulia
      notebook()
      ```
      and you can navigate to and open `lab01.ipynb`.

