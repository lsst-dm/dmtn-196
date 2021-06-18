.. image:: https://img.shields.io/badge/dmtn--196-lsst.io-brightgreen.svg
   :target: https://dmtn-196.lsst.io
.. image:: https://github.com/lsst-dm/dmtn-196/workflows/CI/badge.svg
   :target: https://github.com/lsst-dm/dmtn-196/actions/

#####################################################
Practical, nearly-proper image subtraction, yet again
#####################################################

DMTN-196
========

The "proper image subtraction" of Zackay, Ofek, and Gal-Yam (2016) has theoretical advantages and practical disadvantages compared to Alard & Lupton (1998).  This technote proposes a hybrid; it is not the first such attempt (see DMTN-021 and especially DMTN-179 for very closely related ideas), but it seems to be one not yet considered.

Links
=====

- Live drafts: https://dmtn-196.lsst.io
- GitHub: https://github.com/lsst-dm/dmtn-196

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-dm/dmtn-196

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
