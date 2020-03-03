# AP Generic Cookiecutter

This is a project template powered by [Cookiecutter](https://github.com/cookiecutter/cookiecutter) for use with [datakit-project](https://github.com/associatedpress/datakit-project/).

## Structure

```
.
├── .gitignore
├── README.md
├── analysis
│   └── archive
├── data
│   ├── documentation
│   ├── handmade
│   ├── html_reports
│   ├── processed
│   ├── public
│   └── source
├── etl
├── publish
├── scratch
├── viz
```

- `.gitignore`
  - Ignores a few typical temporary/unnecessary files common to most data projects.
- `README.md`
  - Project-specific readme with boilerplate for data projects.
- `analysis`
  - Code that involves analysis on already-cleaned data. Code for cleaning data should go in `etl`.
  - `analysis/archive`
    - Any analyses for story threads that are no longer being investigated are placed here for reference.
- `data`
  - This is the directory used with our `datakit-data` plugin.
  - `data/documentation`
    - Documentation on data files should go here - data dictionaries, manuals, interview notes.
  - `data/handmade`
    - Manually created data sets by reporters go here.
  - `data/html_reports`
    - Any HTML reports or pages generated by code should go here.
  - `data/processed`
    - Data that has been processed by scripts in this project and is clean and ready for analysis goes here.
  - `data/public`
    - Public-facing data files go here - data files which are 'live'.
  - `data/source`
    - Original data from sources goes here.
- `etl`
  - ETL scripts for transforming source data go here.
- `publish`
  - This directory holds all documents in the project that will be public facing (e.g. data.world documents).
- `scratch`
  - This directory contains scratch materials that will not be used in the project at the end.
  - Common cases are filtered tables or quick visualizations for reporters.
  - This directory is not tracked in git.
- `viz`
  - Graphics and visualization development specific work such as web interactive code should go here.

## Usage

You will need to clone this repository to `~/.cookiecutters/` (make the directory if it doesn't exist):

```
cd path/to/.cookiecutters
git clone git@github.com:associatedpress/cookiecutter-generic-project
```

Then, use `datakit project`:

```
datakit project create --template cookiecutter-generic-project
```

If you'd like to avoid specifying the template each time, you can edit `~/.datakit/plugins/datakit-project/config.json` to use this template by default:

```
{"default_template": "/Users/lfenn/.cookiecutters/cookiecutter-generic-project"}
```

## Configuration

You can set the default name, email, etc. for a project in the `cookiecutter.json` file.