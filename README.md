# About

Test 

This repository is for learnr modules produced by Monash EBS, and submitted for listing on learnr.academy.

## Instructions for Contributors

Please fork this repository and submit a pull request with your module(s) added. Follow either the basic or advanced module structure specified below.

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

## Forking and Contributing Guide

Instructions generated with GitHub copilot on 29, May 2024, then edited and included for reference only.

### Set up development branch

1. **Fork the Repository**: Click on the 'Fork' button at the top right corner of this repository. This will create a copy of this repository in your GitHub account.

2. **Clone the Repository**: Now, clone the forked repository to your machine. Go to your GitHub account, open the forked repository, click on the 'Code' button and then click the 'copy to clipboard' icon to get the URL. Open a terminal and run the following git command:

```bash
git clone "url you just copied"
```

3. **Create a New Branch for your Module**: Change to the repository directory on your computer (if you are not already there):

```bash
cd repository-name
```

Now create a new branch using the `git checkout` command:

```bash
git checkout -b your-new-branch-name
```

### Develop your Modules

4. **Add your module files and Commit**: Now you can make changes in the source code. After you've made your changes, stage them for commit:

```bash
git add .
```

Now commit those changes:

```bash
git commit -m "commit message"
```

5. **Push your Changes to GitHub**:

Push your changes to your Forked repository on GitHub.com using the command `git push`:

```bash
git push origin <your-branch-name>
```

### Submit a Pull Request

Once you are finished developing your module and have pushed it back to your forked repository, you can submit a pull request to the main `numbats/monash-learnr-modules/` repository.

6. **Submit your Changes for Review**: If you go to your repository on GitHub, you’ll see a `Compare & pull request` button. Click on that button. Now submit the pull request.

7. **Wait for Your Changes to be Reviewed**: Once you have submitted your pull request, your changes will be reviewed. If your changes are approved, they will be merged into the main codebase. If your changes are not approved, you will receive feedback and requests for changes.
