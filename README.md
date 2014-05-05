ArcheoloGit
===========

Where should you focus the maintenance efforts? ArcheoloGit is a visualization of age and dev activity for software, powered by d3.js.

# Installation

* clone the project

    git clone git@github.com:marmelab/ArcheoloGit.git
    cd ArcheoloGit

* run the `run.sh` script with the path of the project you want to analyze as argument.

    ./run.sh /path/to/project

* install server dependencies using Bower

    bower install

* run a simple local server on the root, for instance with SimpleHttpServer:

    python -m SimpleHTTPServer .

* browse to the index, for instance [http://0.0.0.0:8000/](http://0.0.0.0:8000/) if you use SimpleHttpServer

![angular.js ArcheoloGit]()

# Usage

ArcheoloGit displays all the files of the project as a rectangle. The size of each rectangle is proportional to the number of commits, the color is green if the file was recently modified, red if it hasn't been modified for a long time.

Therefore:

1. Large red rectangles show files modified often, but untouched for a long time. These are the files you should dig in first for refactoring.
2. Small red rectangles show files seldom modified, and untouched for a long time. These files require your attention, because they could contain hidden bombs.
3. Small green rectangles show files seldom modified, but created or modified recently. They won't need refactoring for now.
4. Large green rectangles show files modified a lot of times, including recently. They probably don't deserve maintenance attention.

You can see the details of a file by hovering the mouse.

If there is too many elements and the graph is not usable, you can change the max depth and then browse the file tree. To go inside a folder, simply click on it. To go back to its parent, click on the `Back` button or press the left direction key.
