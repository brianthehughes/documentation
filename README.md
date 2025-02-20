GhostBSD documentation portal
=============================

Changes committed here trigger an automated build that results in an update to the portal: 

* https://ghostbsd-documentation-portal.readthedocs.io/

Automation involves Sphinx, MyST-parser, Markdown, and a hook with the portal.

## Set up the local development server

Use a local development server that regenerates the output whenever the input changes:

```
git clone https://github.com/ghostbsd/documentation
sudo pkg install -y py311-pip py311-sphinx py311-myst-parser py311-sphinx_rtd_theme gmake rust
pip install docutils
pip install sphinx-autobuild
```

## Start the local development documentation portal

```
cd documentation
sphinx-autobuild source build/html
```

Open http://127.0.0.1:8000/index.html in a web browser.

The documentation portal is regenerated when files are changed. Refresh your web browser to force load of changes.

## Manual documentation generation

One can also generate documentation, in various output formats, locally:

```
gmake html
gmake epub

```
