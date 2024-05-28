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

To preview your module as part of the listing website, run: `quarto preview modules/`.

Your module should appear automatically on the website index page. You can then click through to the preview of your module.