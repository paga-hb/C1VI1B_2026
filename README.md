# Data Visualization (C1VI1B) Autumn 2026

This is the repository for the Data Visualization (Autumn 2026) course at Borås University.

The course schedule can be found on [Kronox](https://schema.hb.se/setup/jsp/Schema.jsp?startDatum=2026-09-01&intervallTyp=a&intervallAntal=1&sprak=EN&sokMedAND=true&forklaringar=true&resurser=k.C1VI1B-20262-I20H6-) and the course material can be found on [Canvas](https://hb.instructure.com/courses/11981).

## Delopment Environment Setup

First, make sure you have installed Visual Studio Code, Git, and Miniconda on your computer.

### Software

Install the following software on your computer:

- [Visual Studio Code](https://code.visualstudio.com)
- [Git](https://git-scm.com/downloads)
- [Miniconda](https://docs.anaconda.com/miniconda/install/#quick-command-line-install)
- [Python](https://www.python.org) (optional) - comes pre-installed on Linux and Mac

### Verify the Software Installation

Verify the software has been successfully installed, by opening a terminal and issuing the following commands (each command should print out a version):

- `code --version`
- `git --version`
- `conda --version`

If you don't see the print-out of a version for a specific tool, make sure the path to your tool's folder has been added to your [`PATH` environment variable](https://gist.github.com/nex3/c395b2f8fd4b02068be37c961301caa7).

### Visual Studio Code (VSCode) Extensions

Then install the necessary Visual Studio Code Extensions by executing the commands below in your terminal:

- `code --install-extension ms-toolsai.jupyter`
- `code --install-extension ms-python.python`

### Accounts

Create a GitHub account (if you don't already have one):

- Visit the [GitHub](https://github.com) web site and [Sign up](https://github.com/signup) for an account.

## Course Repository

When you have installed the software above, open a terminal and clone the GitHub repository [C1VI1B_2026](https://github.com/paga-hb/C1VI1B_2026) to your computer, and create a Python environment:

- `git clone https://github.com/paga-hb/C1VI1B_2026.git dataviz`
- `cd dataviz`
- `conda create -y -p ./.conda python=3.12`
- `conda activate ./.conda`
- `python -m pip install --upgrade pip`
- `pip install ipykernel jupyter pylance numpy pandas matplotlib seaborn bokeh plotly pillow`
- `pip install dash dash-bootstrap-components openpyxl lxml pycountry ipympl basemap pillow kaleido`

## Open the First Workshop Notebook

Finally, make sure you are in the `dataviz/` folder in your terminal, and open the first notebook in Visual Studio Code, by issuing the command below:

- `code -g workshop1/vscode.ipynb:0 .`

When the notebook opens in VSCode, click the text `Select Kernel` (in the top-right of the notebook), and choose `Python Environments... => conda (Python 3.12) .conda/bin/python`.

Now you can follow the instructions in the notebook.

---

## Appendix - Development Environment Setup per Operating System

### Windows
Open an Administrator CMD terminal and issue the commands below:
- Visual Studio Code (VSCode)
  ```bash
  winget install --id Microsoft.VisualStudioCode -e --silent --accept-package-agreements --accept-source-agreements
  ```
- Git (replace "Your Name" and "your.email@example.com" with your name and email address)
  ```bash
  winget install --id Git.Git -e --silent --source winget
  git config --global user.name "Your Name"
  git config --global user.email "your.email@example.com"
  git config --global init.defaultBranch main
  ```
- Miniconda
  ```bash
  winget install --id Anaconda.Miniconda3 -e --silent --accept-package-agreements –accept-source-agreements
  %USERPROFILE%\\miniconda3\\Scripts\\conda init
  %USERPROFILE%\\miniconda3\\Scripts\\conda config --set auto_activate_base false
  ```
- Python (optional)
  ```bash
  winget install --id Python.Python.3 --source winget
  ```
### Mac
Open a terminal and issue the commands below:
- XCode
  ```bash
  touch /tmp/.com.apple.dt.CommandLineTools.installondemand.in-progress
  softwareupdate -i "$(softwareupdate -l | grep -B 1 "Command Line Tools" | awk -F"*" '/^ *\*/ {print $2}' | sed -e 's/^ *//' | tail -n1)"
  ```
- Homebrew
  - On Apple Sillicon (M1,M2,M3, etc.) Mac
    ```bash
    NONINTERACTIVE=1 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
    eval "$(/opt/homebrew/bin/brew shellenv)"
    ```
  - On Intel Mac
    ```bash
    NONINTERACTIVE=1 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    echo 'eval "$(/usr/local/bin/brew shellenv)"' >> ~/.zprofile
    eval "$(/usr/local/bin/brew shellenv)"
    ```
- Visual Studio Code (VSCode)
  ```bash
  brew install --cask visual-studio-code
  ```
- Git (replace "Your Name" and "your.email@example.com" with your name and email address)
  ```bash
  brew install git
  git config --global user.name "Your Name"
  git config --global user.email "your.email@example.com"
  git config --global init.defaultBranch main
  ```
- Miniconda
  - On Apple Sillicon (M!,M2,M3,etc.) Mac
    ```bash
    curl -LO https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh
    bash Miniconda3-latest-MacOSX-*.sh -b -p $HOME/miniconda
    rm Miniconda3-latest-MacOSX-*.sh
    echo 'export PATH="$HOME/miniconda/bin:$PATH"' >> ~/.zprofile
    source ~/.zprofile
    conda init
    conda config --set auto_activate_base false
    ```
  - On Intel Mac
    ```bash
    curl -LO https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
    bash Miniconda3-latest-MacOSX-*.sh -b -p $HOME/miniconda
    rm Miniconda3-latest-MacOSX-*.sh
    echo 'export PATH="$HOME/miniconda/bin:$PATH"' >> ~/.zprofile
    source ~/.zprofile
    conda init
    conda config --set auto_activate_base false
    ```
### Linux (Debian-based Distributions)
Open a terminal and issue the commands below:
- Visual Studio Code (VSCode)
  ```bash
  sudo apt update && sudo apt install -y wget gpg software-properties-common apt-transport-https
  wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
  sudo install -o root -g root -m 644 packages.microsoft.gpg /usr/share/keyrings/
  sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packages.microsoft.gpg] \
  https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
  sudo apt update && sudo apt install -y code
  ```
- Git (replace "Your Name" and "your.email@example.com" with your name and email address)
  ```bash
  sudo apt install git
  git config --global user.name "Your Name"
  git config --global user.email "your.email@example.com"
  git config --global init.defaultBranch main
  ```
- Miniconda
  ```bash
  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh
  bash miniconda.sh -b -p $HOME/miniconda3
  rm miniconda.sh
  ~/miniconda3/bin/conda init
  ~/miniconda3/bin/conda config --set auto_activate_base false
  source ~/.bashrc
  ```
- Python (optional)
  ```bash
  sudo ln -s /usr/bin/python3 /usr/bin/python
  sudo apt install -y python3-pip
  ```
