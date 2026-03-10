# 06 — Opening & Running Jupyter Notebooks
### Python Development | MCC BSIT 2526

[Back to Setup Overview](./Setup.md)

---

Jupyter Notebooks (`.ipynb` files) are the main format for lectures and exercises in this course. You can open and run them in three ways — choose the one that works for your situation.

For theory-heavy topics, recordings and supplementary material are posted on **MS Teams**. The notebooks on GitHub are for code-focused lectures and exercises.

| Action | What to use |
|--------|------------|
| Reading lecture notebooks | Clone the main repo — or open via Binder |
| Submitting exercise notebooks | GitHub Classroom assignment link — always |

These are kept separate. Never submit exercises to the main repo.

---

## Getting the Lecture Notebooks

All lecture notebooks live in the main course repo. Clone it once at the start of the semester and you have everything:

```bash
git clone https://github.com/mcc-bsit-2526/Python-Development.git
```

Open the cloned folder in VS Code and all notebooks are there. When new modules are added, pull the latest:

```bash
git pull
```

If you cannot clone or install anything, use the Binder badge in the repo README — it opens the full notebook environment in your browser with no account and no install required. Note that Binder does not save your work, so use it for reading lecture notebooks only.

---

## Which Option Should I Use?

```
Do you have VS Code + Python installed?
        |
        YES → Option A — VS Code Local (recommended)
        |
        NO
        |
        Do you have a GitHub account?
        |
        YES → Option B — GitHub Codespaces
        |     (VS Code in your browser, work is saved)
        |
        NO or Codespaces not working
        |
        → Option C — Google Colab
          (needs a Google account, extra steps to submit)

```

All three options open the same `.ipynb` file and run the same Python code. The difference is only where the code runs.

---

## Option A — VS Code (Local, Recommended)

Best experience. Code runs on your laptop. Push to GitHub directly.

### Opening a Notebook

1. Open VS Code
2. Open your repo folder: `File → Open Folder` → select your cloned repo
3. In the Explorer panel (left sidebar), click `M01_Exercises.ipynb`

### Selecting a Kernel

The kernel is the Python version that runs your code. Select it once per notebook.

1. Click **"Select Kernel"** in the top right corner of the notebook
2. Choose **"Python Environments"**
3. Select your installed Python (e.g. `Python 3.14.x`)
4. If you are using a virtual environment, select the one inside your project folder

> ⚠️ If no Python version appears, make sure Python is installed and VS Code has been restarted after installing the Python extension.

### Running Cells

| Action | How |
|--------|-----|
| Run one cell | Click the play button on the left of the cell |
| Run one cell (keyboard) | Click inside the cell, press `Shift + Enter` |
| Run all cells | Click "Run All" in the toolbar |
| Stop a running cell | Click the stop button in the toolbar |
| Clear all output | Click "Clear All Outputs" in the toolbar |

### Submitting

Push directly from VS Code. See [07-Submit-Push.md](./07-Submit-Push.md).

---

## Option B — GitHub Codespaces (Online, No Install)

Full VS Code running in your browser, connected directly to your assignment repo. Works on any device including Chromebooks.

**Requirements:** A GitHub account (you already have one from GitHub Classroom)  
**Free limit:** 60 hours per month — sufficient for a full semester

### Opening Your Assignment in Codespaces

1. Go to your assignment repo on GitHub
2. Click the green **Code** button
3. Click the **Codespaces** tab
4. Click **"Create codespace on main"**
5. Wait about 30 seconds — VS Code opens in your browser
6. Click `M01_Exercises.ipynb` in the Explorer panel
7. Select your kernel when prompted

Your work is auto-saved in the Codespace. You can close the browser and return later.

### Submitting from Codespaces

Open the terminal and run:
```bash
git add .
git commit -m "Completed M01 exercises"
git push
```

Or use the Source Control panel in the left sidebar — same as local VS Code.

### Stopping a Codespace

Stop it when done to preserve your free hours:
1. Go to `github.com/codespaces`
2. Find your active Codespace
3. Click the `...` menu → Stop codespace

---

## Option C — Google Colab (Online, Any Device)

Works on any device with a browser and a Google account. No installation required.

**Requirements:** A Google account  
**Free limit:** None for basic use

> ⚠️ Colab disconnects after approximately 90 minutes of inactivity. Save your work often with `Ctrl + S`.

### Opening the Lecture Notebook

1. Go to the course repo on GitHub: `https://github.com/mcc-bsit-2526/Python-Development`
2. Navigate to the module folder
3. Click the **"Open in Colab"** button in the README
4. To save an editable copy: **File → Save a copy in Drive**

### Opening Your Assignment Notebook

1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Click **File → Open notebook**
3. Click the **GitHub** tab and sign in to GitHub
4. Paste your repo URL and press Enter
5. Click `M01_Exercises.ipynb`
6. Click **"Copy to Drive"** at the top to save your own editable copy

### Running Cells in Colab

| Action | How |
|--------|-----|
| Run a cell | Click the play button, or `Shift + Enter` |
| Run all cells | Runtime → Run all |
| Restart kernel | Runtime → Restart runtime |
| Clear outputs | Edit → Clear all outputs |

### Submitting from Colab

Colab cannot push to GitHub directly. Follow these steps:

1. Finish your work in Colab
2. File → Download → Download `.ipynb`
3. Go to your assignment repo on GitHub
4. Click **Add file → Upload files**
5. Upload your downloaded `.ipynb` file
6. Type a commit message, e.g. `Completed M01 exercises via Colab`
7. Click **Commit changes**

The autograder runs automatically after your commit.

---

## Understanding Cell Types

All three options use the same notebook format with two cell types:

**Markdown cells** — text cells with instructions and explanations. Read these carefully. You cannot run them.

**Code cells** — Python code you can edit and run. Output appears below the cell after running. These are where you write your answers.

---

## Your Workflow for Every Exercise

```
1. Read the Markdown cell (instructions)
2. Click the Code cell below it
3. Write your Python code
4. Press Shift + Enter to run
5. Check the output
6. Fix and re-run if needed
7. Move to the next exercise
```

---

## Adding Test Cells

You can add extra code cells anywhere to test your work — this does not affect your grade. The autograder only checks the specific functions in the exercise cells.

Hover between two cells and click **"+ Code"** to insert a new cell.

---

## Option D — Binder (Read-Only, No Account)

Binder opens the course repo as a live JupyterLab environment in your browser. No account, no install, no setup.

**Use this for:** Reading and running lecture notebooks when you have no other option  
**Do not use this for:** Exercise notebooks — Binder does not save your work

Click the Binder badge in the course repo README to launch. It takes 1–2 minutes to build on first load.

> ⚠️ Any work done in Binder is lost when you close the tab or the session times out. Never write your exercise answers here.

---

## Comparison

| | Option A | Option B | Option C | Option D |
|--|---------|---------|---------|---------|
| **Where it runs** | Your machine | GitHub servers | Google servers | Binder servers |
| **Account needed** | No | GitHub | Google | None |
| **Install needed** | Yes | No | No | No |
| **Saves work** | Yes | Yes | Yes (Google Drive) | No |
| **Push to GitHub** | Direct | Direct | Manual upload | No |
| **Works for exercises** | Yes | Yes | Yes | No |
| **Works for game dev** | Yes | Terminal only | No | No |
| **Recommended** | Main setup | Official fallback | Last resort | Lecture reading only |

---

## Common Issues

**VS Code — "No kernel found"**  
Click "Select Kernel" (top right) → Python Environments → pick your Python version.

**Codespaces — takes too long to load**  
Wait up to 2 minutes on first creation. If it times out, refresh and try again.

**Codespaces — "You have no Codespaces"**  
Make sure you are signed into the same GitHub account used for Classroom.

**Colab — "Runtime disconnected"**  
Click Reconnect, then re-run all cells from the top since Colab clears memory on disconnect.

**Colab — cannot find the GitHub tab**  
Go to [colab.research.google.com](https://colab.research.google.com) → File → Open notebook → GitHub → sign in when prompted.


**Binder — takes forever to load**  
Binder can take up to 5 minutes if the environment has not been built recently. If it fails, try again once. If it keeps failing, use Colab instead.

For more issues, see [08-Troubleshooting.md](./08-Troubleshooting.md).

---

Next: [Submit Your Work](./07-Submit-Push.md)
