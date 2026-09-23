# Urban Computing Assignment 2

This repository contains the second assignment for the Urban Computing course in Fall 2026.

The exercises can be found in *"Assignment_2_SpatialData.ipynb"*. The file *"lab_04_modified.ipynb"* is used in Task 3.

The completed assignment must be submitted through **Brightspace** as described in the *Submission procedure* section below.

## Installation

We will use Visual Studio Code (VS Code) as the IDE for this assignment.

Two setup options are supported:

1. **Development Container (Docker)**
2. **Python virtual environment (`venv`)**

Both options are suitable for completing the assignment. You may use whichever works best on your own computer.

### Clone the repository

Make sure you have [Git](https://git-scm.com/downloads) and [VS Code](https://code.visualstudio.com/) installed.

Clone the Assignment 2 repository to your computer:

```bash
git clone https://github.com/UC-Course-LU/Assignment2.git
```

Then move into the repository folder:

```bash
cd Assignment2
```

Open the repository in VS Code:

```bash
code .
```

Cloning the repository creates a local copy of the assignment files on your computer. Work inside this cloned folder so that the notebook, data files, `requirements.txt`, and any other provided files remain in the expected folder structure.

---

## Option 1: Development Container (Docker)

**Note:** Installing Docker may require administrator rights.

### Required software

- [Docker](https://docs.docker.com/get-docker/)
- [Visual Studio Code](https://code.visualstudio.com/)
- The **Dev Containers** extension for VS Code

If you are running Linux, follow Docker's additional post-installation step for [managing Docker as a non-root user](https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user).

### Open the assignment in the development container

1. Open the cloned Assignment 2 repository in VS Code.
2. Open the **Extensions** panel.
3. Search for **Dev Containers** and install the extension.
4. In the bottom-left corner of VS Code, click the remote window / connection indicator.
5. Select **Reopen in Container**.

Alternatively, open the Command Palette:

- Windows/Linux: `Ctrl+Shift+P`
- macOS: `Cmd+Shift+P`

Then select:

```text
Dev Containers: Reopen in Container
```

VS Code will build the container and reopen the repository inside it. The first build may take some time.

If you need to rebuild the environment later, use:

```text
Dev Containers: Rebuild Container
```

Once the container is ready, open *"Assignment_2_SpatialData.ipynb"* and start working on the assignment.

---

## Option 2: Python virtual environment (`venv`)

You can also run the assignment locally using a standard Python virtual environment.

### Windows

Create the virtual environment:

```powershell
python -m venv .venv
```

Activate it:

```powershell
.venv\Scripts\Activate.ps1
```

### macOS / Linux

Create the virtual environment:

```bash
python3 -m venv .venv
```

Activate it:

```bash
source .venv/bin/activate
```

### Install the dependencies

After activating the environment, run:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Then open the repository in VS Code and open *"Assignment_2_SpatialData.ipynb"*.

Select the Python interpreter from the `.venv` environment as the notebook kernel.

If needed:

1. Open the notebook.
2. Click **Select Kernel** in the top-right corner.
3. Select the Python interpreter from `.venv`.

The provided `requirements.txt` includes `ipykernel`, which allows the virtual environment to be used as a Jupyter notebook kernel in VS Code.

---

## Submission procedure

The assignment must be submitted through **Brightspace** before **October 20th at 23:59**.

Before submitting, rename your completed notebook using your student number.

For example:

```text
s1234567.ipynb
```

Run the notebook from beginning to end before submission and save it after execution.

### Notebook outputs are required

**Do not clear the notebook outputs before submission.**

All code cells must remain visible together with their outputs so that your results can be inspected during grading.

You must also export an HTML version of the final executed notebook.

For example:

```text
s1234567.html
```

The HTML file must correspond to the same final version of the notebook that you submit.

### Files to submit

Create **one ZIP file** named using your student number, for example:

```text
s1234567_Assignment2.zip
```

The ZIP file must contain:

- `s1234567.ipynb` — your completed notebook, including all outputs
- `s1234567.html` — the HTML export of the completed notebook
- `requirements.txt` — containing the Python packages and versions used for your solution

Upload this ZIP file to **Brightspace** before the deadline, October 20th.

Do **not** include unnecessary files such as:

- `.venv/`
- `.git/`
- `__pycache__/`
- Docker images or containers
- cache files
- unchanged assignment files that were already provided

---

## Updating `requirements.txt`

Before submission, make sure you are working inside the Python environment that you actually used for the assignment, either:

- the development container, or
- your `.venv` virtual environment.

Do **not** run the following command from your system/global Python environment.

Run:

```bash
python -m pip freeze > requirements.txt
```

This records the installed Python packages and their versions so that your environment can be reproduced during grading.

If you install additional Python packages while working on the assignment, make sure the final `requirements.txt` reflects the environment used for your final solution.

---

## Final check

Before creating the ZIP file:

1. Run the notebook from beginning to end and make sure it completes without errors.
2. Save the notebook after running it.
3. Make sure **all notebook outputs are still visible**.
4. Rename the notebook using your student number.
5. Export the final notebook to HTML.
6. Check that the HTML file corresponds to the final notebook.
7. Make sure `requirements.txt` reflects the environment used for the assignment.
8. Create the ZIP file containing the notebook, HTML file, and `requirements.txt`.
9. Upload the ZIP file to Brightspace before the deadline.

---

## Tips

- You can install additional Python packages inside your active environment with:

```bash
python -m pip install <package>
```

- If a package is required for your solution, make sure it is reflected in the final `requirements.txt`.
- A light VS Code theme may be preferred while working with Python notebooks.
  - To change themes: **File/Code → Preferences → Color Theme**.
- If you use the development container and need to install non-Python system packages, update the `.devcontainer/Dockerfile` and rebuild the container.

# References

## Development Containers

- [Beginner's Series to Dev Containers](https://www.youtube.com/watch?v=61M2takIKl8&list=PLj6YeMhvp2S5G_X6ZyMc8gfXPMFPg3O31) on YouTube

## NumPy & Pandas

- [Cloud X Lab - introduction to NumPy and Pandas](https://cloudxlab.com/blog/numpy-pandas-introduction/)
- [Zero With Dot - Performance of NumPy and Pandas - comparison](https://zerowithdot.com/python-numpy-and-pandas-performance/)
- [Sofia Heisler - A Beginner’s Guide to Optimizing Pandas Code for Speed](https://engineering.upside.com/a-beginners-guide-to-optimizing-pandas-code-for-speed-c09ef2c6a4d6)
- [Pandas - Enhancing Performance](https://pandas.pydata.org/pandas-docs/stable/user_guide/enhancingperf.html)
- [Numexpr](https://github.com/pydata/numexpr)
- [Real Python - Look Ma, No For-Loops: Array Programming With NumPy](https://realpython.com/numpy-array-programming/)
- [Python Like You Mean It - Vectorized Operations](https://www.pythonlikeymeanit.com/Module3_IntroducingNumpy/VectorizedOperations.html)

## Matplotlib

- [Real Python - Python Plotting With Matplotlib (Guide)](https://realpython.com/python-matplotlib-guide/)
- [Practical Business Python - Effectively Using Matplotlib](https://pbpython.com/effective-matplotlib.html)
