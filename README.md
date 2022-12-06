# latex Resume

## Setup

1. On Mac, install `maclatex` with:

    ```bash
    brew install --cask mactex
    ```

1. In VSCode, install LatexWorkshop extension from marketplace
1. In vscode, add this in `settings.json` to allow using xelatex which this needs.

    ```json
    "latex-workshop.latex.tools": [
        {
            "name": "latexmk",
            "command": "latexmk",
            "args": [
                "-xelatex",
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ]
        }
    ]
    ```

1. Restart vscode
1. In latext `.tex` file, add line

    ```bash
    % !TEX root = ./<TEX_FILENAME>.tex
    ```

1. On each save of .tex file, it will attempt to build PDF. Look at TEX section at left pane or Output terminal for any compile errors.
