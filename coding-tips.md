# Coding Tips

[Back](index.md)

## Table of Contents

[Installation](#installation)

## Installation

### PowerShell

1. Open PowerShell

2. Open the profile file

    ``` PowerShell
    notepad $PROFILE
    ```

3. Add the following commands and save the profile file.

    ```PowerShell
    $Env:github = "C:\Users\wonja\Documents\GitHub"
    $Env:python = "C:\Users\wonja\Documents\Python"
    $Env:r = "C:\Program Files\R\R-4.0.5\bin\x64"
    $Env:d3 = "C:\Users\wonja\Documents\GitHub\D3"
    $Env:julia = "C:\Users\wonja\Documents\Julia"
    Set-Location -Path "C:\Users\wonja\Documents\GitHub"
    ```

4. Restart PowerShell

### Python

1. Install the latest version from <https://www.python.org/>.

2. Open PowerShell

3. Create a new virtual environment.

    ```PowerShell
    python -m venv C:\Users\wonja\Documents\Python\39
    ```

4. Create a new requirements file in the environment directory.

    ```PowerShell
    notepad C:\Users\wonja\Documents\Python\39\requirements.txt
    ```

5. Add the following requirement specifiers and save the requirements file.

    ```text
    numpy
    pandas
    matplotlib
    statsmodels
    linearmodels
    jupyterlab
    jupyter-book
    Flask
    ```

6. Activate the environment.

    ```PowerShell
    C:\Users\wonja\Documents\Python\39\Scripts\activate.ps1
    ```

7. Install packages from the requirements file.

    ```PowerShell
    pip install -r C:\Users\wonja\Documents\Python\39\requirements.txt
    ```

8. Upgrade packages from the requirements file.

    ```PowerShell
    pip install -U -r C:\Users\wonja\Documents\Python\39\requirements.txt
    ```

### R

1. Install the latest version from <https://www.r-project.org/>

2. Open PowerShell

3. Activate the python environment.

    ```PowerShell
    C:\Users\wonja\Documents\Python\39\Scripts\activate.ps1
    ```

4. Open RGui.

    ```PowerShell
    & "C:\Program Files\R\R-4.0.5\bin\x64\RGui.exe"
    ```

5. Install the IRkernel package.

    ```R
    install.packages("IRkernel")
    ```

6. Install a kernel spec.

    ```R
    IRkernel::installspec()
    ```

7. Install the latest version of RStudio from <https://www.rstudio.com/>

8. Open RStudio from the start menu.

9. Install the renv package.

    ```R
    install.packages("renv")
    ```

10. Initialize a new project.

    ```R
    renv::init(project = "C:/Users/wonja/Documents/R/40", bare = TRUE)
    ```

11. Install the following packaages.

    ```R
    install(c("tidyverse", "lfe", "tidymodels", "rmarkdown", "bookdown", "shiny"))
    ```

12. Update the following packaages.

    ```R
    update(c("tidyverse", "lfe", "tidymodels", "rmarkdown", "bookdown", "shiny"))
    ```

### Julia

1. Install the latest version from <https://julialang.org/>

2. Open PowerShell.

3. Activate the python environment.

    ```PowerShell
    C:\Users\wonja\Documents\Python\39\Scripts\activate.ps1
    ```

4. Create a new project directory.

    ```PowerShell
    New-Item -Path "C:\Users\wonja\Documents\Julia\" -Name "16" -Itemtype "directory"
    ```

5. Set location to the new project directory.

    ```PowerShell
    Set-Location -Path "C:\Users\wonja\Documents\Julia\16\"
    ```

6. Open Julia

    ```PowerShell
    C:\Users\wonja\AppData\Local\Programs\Julia-1.6.1\bin\julia.exe
    ```

7. Enter the Pkg REPL by pressing `]`.

8. Install the IJulia package.

    ```Julia
    add IJulia
    ```

9. Activate the project.

    ```Julia
    activate .
    ```

10. Install the following packages.

    ```Julia
    add StatsKit
    ```

11. Update the following packages.

    ```Julia
    up StatsKit
    ```

12. Exit Julia and open the settings file in the IJulia kernel directory.

    ```PowerShell
    notepad C:\Users\wonja\AppData\Roaming\jupyter\kernels\julia-1.6\kernel.json
    ```

13. Add the following command to `argv` and save the settings file.

    ```text
    "--project=C:\\Users\\wonja\\Documents\\Julia\\16",
    ```

### Visual Studio Code

1. Install the latest version from <https://code.visualstudio.com/>

2. Install the following extensions.

    * Python from Microsoft
    * Jupyter from Microsoft
    * Prettier from Prettier
    * Visual Studio IntelliCode from Microsoft
    * SQL Server from Microsoft
    * PowerShell from Microsoft
    * markdownlint from David Anson
    * Julia from julialang

### GitHub

1. Create a new repository.

2. Navigate to the main page of the repository.

3. Above the list of files, click `Code`.

4. Copy HTTPS URL.

5. Open PowerShell

6. Set location to the parent directory of the repository.

7. Clone the repository.

    ```Git
    git clone h<span></span>ttps://github.com/wonjae-lee-2/DEDP.git
    ```

8. Create `.vscode` subfolder in the repository.

9. Create `settings.json` in the subfolder with the following commands.

    ```json
    {
        "python.pythonPath": "C:\\Users\\wonja\\Documents\\Python\\39\\Scripts\\python.exe",
        "julia.environmentPath": "c:\\Users\\wonja\\Documents\\Julia\\16"
    }
    ```