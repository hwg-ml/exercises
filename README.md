# C29331 Machine Learning

![Header](./docs/header.png)

Welcome to the C29331 Machine Learning repository! This project is aimed to assist you in working on the exercises. 

## Prerequisites
We will be working with many tools throughout this lecture that are considered
to be in the standard tool kit of a developer. However, universities typically
spend little time on teaching these fundamentals. I can therfore only
highly recommend the [Missing Semester MIT Course](https://missing.csail.mit.edu) which tries to fill this gap as we won't have time to discuss these topics in depth.

### Terminal

![](/docs/terminal.png)

You will need to work with your terminal to get these tools installed. The terminal is a mighty and powerful tool, but we will only use it sparsely. Please make yourself at least familiar with the commands from [this blog](https://mrkaluzny.com/blog/terminal-101-getting-started-with-terminal/). The MIT course includes a [lecture dedicated to the terminal](https://missing.csail.mit.edu/2026/course-shell/) if you want to learn more.

### Git

Make sure you have [Git](https://git-scm.com/) installed on your machine. You can download it from the official website and follow the installation instructions for your operating system using the [official guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). You can verify the installation worked by typing `git`in your terminal. The output should be similiar to this:

![git](/docs/git.png)
### Visual Studio Code

We will be working with [Visual Studio Code](https://code.visualstudio.com/) as our code editor. If you haven't installed it yet, please download and install it from the official website. It will also work with other IDEs, but I can only provide support for VS Code.

### UV

We will be using [UV](https://docs.astral.sh/uv/) to manage our python environment. Please download and install it on your device using the official [installation guide](https://docs.astral.sh/uv/getting-started/installation/).


## Cloning the Repository

Clone the repository to your local machine using the following command in your terminal:

```bash
git clone https://github.com/hwg-ml/exercises.git hwg-ml-exercises
```
Navigate into the cloned directory:

```bash
cd hwg-ml-exercises
```

## Setting Up the Environment

Create a new Python environment and install the pinned dependencies from `pyproject.toml` and `uv.lock` with:

```bash
uv sync
```

UV will create a local virtual environment (usually at `.venv/` inside the project) and install all required packages. After `uv sync` you can:

- Let VS Code pick the `.venv` interpreter (see the next section), or
- Activate manually in a terminal: `source .venv/bin/activate` (macOS / Linux) and then run notebooks or commands.


## Opening Jupyter Notebooks in VS Code

1. Open Visual Studio Code.
2. Install the Python extension for VS Code if you haven't already. You can find it in the Extensions view, search for "Python", and install the one published by Microsoft.
3. Open the cloned repository folder in VS Code by selecting `File > Open Folder` and navigating to the `hwg-ml-exercises` directory.
4. Copy over the exercise files and open the (`hello_world.ipynb`) in the repository.

### Selecting the Python Interpreter

1. On the Top Right Corner of the VS Code window, click on the Python kernel selector. ![Select Interpreter](./docs/select-kernel.png)
2. Click on "Python Environment" ![Select Python Environment](./docs/select-python-environment.png)
3. Select the interpreter that corresponds to the environment you created:

- Choose the `.venv/bin/python` interpreter inside the project folder (the images show this flow). ![Select UV Environment](./docs/choose-venv.png)

If the environment doesn't show up in the list, restart VS Code or open a terminal from VS Code with the env activated and try again.

### Running the Notebooks

You can now run the cells in the Jupyter Notebook by clicking the "Run" button or using the keyboard shortcut `Shift + Enter`.

![Run Notebook](./docs/running-cells.png)

## Working on the Exercises

You will find all exercises on the [course page](https://h4hn.de/courses/c29331-machine-learning). You can either manually copy the unziped folder with the exercise into the `exercises` folder in the repository or you can use the CLI to download them automatically.

### Using the CLI

This repository includes a [command-line-interface (`hwg-ml`)](https://github.com/hwg-ml/cli) for downloading course materials from the course website.

You can run the cli either with an activated environment or using uv:
```sh
# with activated environment
hwg-ml
# without activated environment
uv run hwg-ml
```

### Download Exercises

Download all exercises for the course:

```bash
hwg-ml exercises update 
# or without an active environment
uv run hwg-ml exercises update
```

**Options:**
- `--output` / `-o`: Specify output directory (default: `exercises/`)

### Download Lecture Slides

Download all lecture PDF slides:

```bash
hwg-ml lectures update 
# or without an active environment
uv run hwg-ml lectures update
```

**Options:**
- `--output` / `-o`: Specify output directory (default: `lectures/`)


   
## Turning Off Copilot

If you have GitHub Copilot enabled in VS Code, I recommend you turn it off. Ultimately it is you decision, but if you leave it on, you will not actually learn anything.

1. Open the Command Palette by pressing `Ctrl + Shift + P` (or `Cmd + Shift + P` on macOS).
2. Type "Copilot: Disable Completions" and select the option to disable GitHub Copilot

You may re-enable it later by following the same steps and selecting "Copilot: Enable Completions".
