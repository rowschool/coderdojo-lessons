# Contributing

At CoderDojoKC, we would like to provide a nice way for the community to help improve our lessons.

## Code of Conduct

We follow the [CoderDojo Charter](https://zen.coderdojo.com/charter) and adhere to the [Kansas City Women in Technology Code of Conduct](https://kansascitywomenintechnology.github.io/CodeOfConduct/)

## Text Markup

This project uses two different kinds of text markup:

* [Markdown](https://daringfireball.net/projects/markdown/)
* [restructuredText](http://docutils.sourceforge.net/rst.html)

If you're writing something without images or tables, you can use Markdown. It provides an easy and quick way to create formatted text with lists and nicely formatted code examples. Here is a good [Markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

If you're writing something with images or tables, please write it using restructuredText. RestructuredText uses a semantic markup that allows one to create accessible documentation. For instance, if you have an image that requires a licensing notice or a citation, you can more easily create a [caption in restructuredText](https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html#images-and-figures) than you can in Markdown. Here is a good [restructuredText cheatsheet](https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html).

## Building a local version

### Requirements

* Python 3.5 or higher.

### How to

**Get Started:**

1. Fork this repository.
1. Clone this repository to your local development machine: `git clone <your-fork.git>`.
1. Change directory into the directory the new repository: `cd !$`.
1. Create a Python virtual environment for this project: `python3 -m venv venv`. **Note:** Feel free to use whichever tooling you prefer for creating and managing Python virtual environments. The `venv` module has the benefit of being included with Python 3.5 and higher.
1. Activate the Python virtual environment: `source venv/bin/activate`. **Note:** If you are using a different method of managing Python virtual environments, use its command for activating the virtual environment.
1. Install the Python dependencies for this project: `make dev`.

**To build an HTML version of this documentation locally:**

1. `make html`
1. Open `build/html/index.html` in your favorite browser

**To add a Python package:**

1. Edit either `requirements.in` or `requirements-dev.in` (depending on if the package is for use as a project dependency or development dependency) in your favorite text editor and add the name of the package you want to add.
1. Run `make requirements` to add it to the `requirements.txt` or `requirements-dev.txt` file.
1. Run `make sync` to bring your Python virtual environment's installed packages up to date with the newly updated `requirements*.txt` files.

// todo Making a Pull Request
