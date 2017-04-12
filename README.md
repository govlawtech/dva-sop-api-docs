# dva-sop-api-docs

General documentation for the DVA-SOP-API.

This documentation is built using the Sphinx documentation system.

The source files for the documentation is storedin the **'docsSrc'** directory.

The live (built) documentation files are stored in the **'docs'** directory.
The **'docs'** directory is entirely generated, there should be no need to manually edit anything in it.
If you need to add static resources (e.g. linked PDFs), place them inside the **'docsSrc/_static/resources'** folder

The documentation can be built with 'sphinx-build' as per the example .bat file.
After building, simply commit the changes to the generated **'docs'** directory the documentation will become available at https://govlawtech.github.io/dva-sop-api-docs/

This requires an installation of sphinx from http://www.sphinx-doc.org/en/stable/ and the **sphinx_rtd_theme** (pip install sphinx_rtd_theme)
