# About

This repository is for learnr modules produced by Monash EBS, and submitted for listing on learnr.academy.

## Instructions for Contributors

### Basic Modules

Add your module (e.g. `basic/`) to `modules/` and it should have the following structure:

```
modules/
└── basic/
    └── index.qmd
└── advanced/
    └── index.qmd
```

- `index.qmd` is the main content file for your module.
- You can include other files (e.g. `images/`) in the module directory as needed.

To preview your module as part of the listing website, run: `quarto preview modules/`. Your module should appear automatically on the website index page. You can then click through to the preview of your module.

### Advanced Modules

If your module requires additional resources or specific extensions, add them INSIDE your module folder:
```
modules/
└── basic/
    └── index.qmd
└── advanced/
    ├── resources/         ## anything you need for your index.qmd to render
    │   └── images/
    │   └── data/
    │   └── scripts/
    ├── _extensions/       ## extensions used in your index.qmd
    │   └── quarto-ext/
    │       └── include-code-files/
    │           ├── _extension.yml
    │           └── include-code-files.lua
    └── index.qmd
```

The top level `_extensions` folder should only contain the `quarto-webr-teachr` extension. Do not modify this folder. If you use `quarto add <ext>` to install extensions, you may need to move the extension out of the top level folder.