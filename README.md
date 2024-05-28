# About

This repository is for learnr modules produced by Monash EBS, and submitted for listing on learnr.academy.

## Instructions for Contributors

Add your module (e.g. `basic/`) to `modules/` and it should have the following structure:

```
modules/
└── basic/
    ├── _extensions/
    │   └── quarto-ext/
    │       └── include-code-files/
    │           ├── _extension.yml
    │           └── include-code-files.lua
    └── index.qmd
```

Note that `index.qmd` is the main content file for your module. You can include other files (e.g. `images/`, module specific `_extensions` etc.) in the module directory as needed. The top level `_extensions` folder should only contain the `quarto-webr-teachr` extensions. If you use `quarto add <ext>` to install extensions, you may need to move do not modify this folder.

To preview your module as part of the listing website, run: `quarto preview modules/`.

Your module should appear automatically on the website index page. You can then click through to the preview of your module.