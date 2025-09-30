# ukceh-rse.github.io

This repository contains the [UKCEH RSE group website](https://ukceh-rse.github.io/).


## Building the site *without* the tutorials

It is more straightforward to build the site without the `tutorials` submodule.

First, install [Quarto](https://quarto.org/docs/get-started/) version ≥ 1.8.

Clone the repository _without the tutorials submodule_,

```sh
git clone https://github.com/ukceh-rse/ukceh-rse.github.io
```

In the root of the repository, simply run

```sh
quarto render
```

and open the site in your browser.


## Building the site _with_ the tutorials

In this case you should clone the repository using

```sh
git clone --recurse-submodules https://github.com/ukceh-rse/ukceh-rse.github.io
```

If you already cloned the repository without submodules (`tutorials/` will be empty), you will need to run the following commands:

```sh
git submodule init
git submodule update
```

You will need to render each tutorial individually before rendering the rest of the website. Each tutorial comes with its own set of dependencies, and you will need to consult the tutorial's `README.md` in each case for guidance on rendering.

The good news is that, once a tutorial is rendered, its rendered output is cached and will not need to be re-rendered unless (a) the tutorial is updated, or (b) the rendered outputs in `_site/` or `_freeze/` are deleted.

Once all tutorials are rendered, return to the repository root and run

```sh
quarto render
```


## Contributing

For substantive contributions, e.g. new updates, projects or tutorials, please open a pull request.
For tweaks, corrections etc feel free to simply commit to `develop`.

### Updates

Create a new directory under `updates/`, starting with the date of the update in the form `YYYY-MM-DD`, and a file called `index.qmd` in that directory.

See [this example](https://github.com/ukceh-rse/ukceh-rse.github.io/blob/main/updates/2025-09-04_ml_coupling_workshop/index.qmd).


### Projects

The idea here is for us to write a very short description of a project when we first start it, and upgrade this to a (still short) retrospective account of the project once we are finished.

Create a new directory under `projects/`, starting with the year of the project (`YYYY`), and a file called `index.qmd` in that directory.

Use the `active` category to mark active projects.

See e.g. [this example](https://github.com/ukceh-rse/ukceh-rse.github.io/blob/main/projects/2025_biodt/index.qmd).

### Tutorials

Tutorials are kept in their own repository at [ukceh-rse/tutorials](https://github.com/ukceh-rse/tutorials).

Follow the instructions there to contribute a new tutorial.

