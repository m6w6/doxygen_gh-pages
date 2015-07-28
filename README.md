# Doxygen gh-pages

Runs doxygen on the current checkout into your gh-pages branch.

## Usage:

    cd project.git
    ../doxygen_gh-pages.git/doxypages < Doxyfile
    git push origin gh-pages

## What it does:

* Creates a temporary workdir of the gh-pages branch with git-new-workdir
* Runs doxygen with `OUTPUT_DIRECTORY=$TEMPDIR`
* Commits changes to gh-pages
* Cleans up `$TEMPDIR`

Simple enough, but I didn't want to maintain it in several different repos.

## Prerequisites:

* git
* git-new-workdir
* doxygen


