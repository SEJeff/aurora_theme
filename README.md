Aurora Theme
============

This is a custom theme for the [Apache Aurora documentation](https://aurora.apache.org/documentation/latest) to use the most wonderful [mkdocs](http://mkdocs.org) project for rendering html documentation.

This is an experiment to try and make contributing to Aurora's documentation an easier process.


Requirements
------------

First things first, you'll need a clone of the upstream aurora.git:

    git clone https://git-wip-us.apache.org/repos/asf/aurora

You'll also need to [install mkdocs](http://www.mkdocs.org/#installation):

    pip install mkdocs


Setup
-----

Check out `aurora_theme` into the root of the aurora git checkout.

    cd aurora && git clone https://github.com/SEJeff/aurora_theme

Ensure the configuration file, `mkdocs.yml`, is in the correct place:

    ln -s aurora_theme/mkdocs.yml .


Limitations
-----------

This is really cool, so what gives?

Currently, mkdocs [doesn't support](https://github.com/mkdocs/mkdocs/issues/608) rendering `README.md` as the index page. Move docs/README.md to docs/index.md.

    mv docs/{README,index}.md


Viewing The Documentation
-------------------------

From the root of the aurora git checkout with `aurora_theme` setup start the [mkdocs dev server](http://www.mkdocs.org/#getting-started).

    mkdocs serve

Open up a browser to http://localhost:8000


Rendering to Static HTML
------------------------

Building the documentation is straightforward.

    mkdocs build --clean
