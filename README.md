# Docs

This repo contains the documentation source for: <https://docs.foundries.io>

## About

We write the docs in[reStucturedText](https://docutils.sourceforge.io/rst.html),
with [Sphinx](https://www.sphinx-doc.org/en/master/) serving as the site generator.

We use the [Sphinx PyData Theme](https://pydata-sphinx-theme.readthedocs.io/en/stable/).

## Requirements

Before beginning any work, review the [contributing section](#contributing).

Building the documentation requires python 3.12 or greater.
All required python modules are in `requirements.txt`.
Install them with `pip3 install -r requirements.txt`. _virtual environment recommended_

### Using a Virtual Environment to Provide Requirements

To avoid messing with your system-wide package storage, use `virtualenv`, or the builtin `venv`.
This will set up the necessary environment for sphinx packages and place them here:

```bash

$ sudo apt-get install graphviz python3 python3-virtualenv
$ virtualenv -p /usr/bin/python3 venv
$ . ./venv/bin/activate
$ pip install -r requirements.txt

```

**NOTE:** You may need to specify the python version when initializing the virtual environment.

## Building the Docs Locally

To build the html from rst files, from the top directory run:

```bash

$ make html

```

📌 **NOTE:** When you fork this project, make sure to disable the option that allows forking only the main branch. 
If you overlook this step, you may encounter issues when executing the make html command,
requiring you to specify the value via the environment variables `MP_UPDATE_VERSION`.

Open `build/html/index.html` in your browser to view the
documentation.

Alternatively, you can run `sphinx-autobuild source build` which will start a server at `http://127.0.0.1:8000/index.html`,
and will rebuild the docs when it detects a change.

## Contributing

### Before Working on Documentation

You **must** use a fork rather than working on a `foundriesio/docs` branch.
Branch names should be descriptive and in the imperative (what you *will* do):

```bash
git checkout -b spell-check-everything
```

Before you start, check the default branch to see the if the issue is still relevant.

> The published pages reflect the documentation as of the latest release.
The change may exist and will show up in the next release.

#### Internal Contributions

For internal contributions, check Jira to make sure someone else is not already working on the issue.

> If there is no open issue, should there be one?
If the fix is going to take more than 30 minutes, consider opening one.

#### Public Contributions

We recommend opening an issue on GitHub first; we will likely tell you to go for it!

### Working on Documentation

For new pages, first look for an appropriate template under `templates/`

Use spelling and grammar checks and ask a technical writer if you have questions.
Consult the [style guide](https://foundriesio.atlassian.net/wiki/spaces/ID/pages/2392067/Foundries.io+Style+and+Communication+Guide).

You can also "lint" the document. A GitHub action will also run the linter upon opening a Pull Request (PR).
[Install vale](https://vale.sh/docs/vale-cli/installation/), and from this directory run:

```bash
vale sync
vale <PATH/FILE>
```

:exclamation: make sure you are using Vale 2.16.0 or greater

#### Custom Prev/Next

To configure a page to have a different prev or next link,
add the appropriate metadata to the top of the file:

`:prev_link: <path to page>.html`
`:prev_title: < title of link, can be anything>`

For "next" use `next_link` and `next_title`.

#### Screenshots and Diagrams

Find visual assets in `source/_static`.
Directory structure is `<section>/<subsection>/<image.png>`.
Limit depth should to one nested header. For example:
`getting-started/signup/build.png`

Any image used by the theme, such as the logo, goes directly under `_static`.

If using an image more than once, place it in the section folder which appears first in the ToC.


#### Opening a Pull Request

Open your PR against the `next` branch. Once approved and merged by a maintainer,
the changes will be published  to the [dev version](https://docs.foundries.io/dev).

Before pushing, check locally:

- links; `make linkcheck`
- html; `make html`
- lint: `vale <path_to_file(s)>`

When opening a PR, add "documentation team" for your reviewer if possible.
For any changes that reflect changes to how the FoundriesFactory™ Platform is used/interacted with—the majority—please add the Customer Success team.
Someone from the documentation team will merge it once reviews are in and suggestions considered.
The [PR template](.github/pull_request_template.md) has additional steps that can speed up the process.

