Welcome to the ZooKeeper documentation!

This readme will walk you through navigating and building the ZooKeeper documentation, which is included
here with the ZooKeeper source code. You can also find documentation specific to release versions of
ZooKeeper at http://zookeeper.apache.org/documentation.html.

Read on to learn more about viewing documentation in plain text (i.e., markdown) or building the
documentation yourself. Why build it yourself? So that you have the docs that corresponds to
whichever version of ZooKeeper you currently have checked out of revision control.

## Prerequisites

The ZooKeeper documentation build uses a number of tools to build HTML docs.

You need to have [Ruby](https://www.ruby-lang.org/en/documentation/installation/) and
[Python](https://docs.python.org/2/using/unix.html#getting-and-installing-the-latest-version-of-python)
installed. Also install the following libraries:

```sh
$ sudo gem install jekyll jekyll-redirect-from pygments.rb
$ sudo pip install Pygments
```

(Note: If you are on a system with both Ruby 1.9 and Ruby 2.0 you may need to replace gem with gem2.0)

## Generating the Documentation HTML

We include the ZooKeeper documentation as part of the source (as opposed to using a hosted wiki, such as
the github wiki, as the definitive documentation) to enable the documentation to evolve along with
the source code and be captured by revision control (currently git). This way the code automatically
includes the version of the documentation that is relevant regardless of which version or release
you have checked out or downloaded.

In this directory you will find text files formatted using Markdown, with an ".md" suffix. You can
read those text files directly if you want. Start with `index.md`.

Execute `jekyll build` from the `src/docs/` directory to compile the site. Compiling the site with
Jekyll will create a directory called `_site` containing `index.html` as well as the rest of the
compiled files.

```sh
$ cd src/docs
$ jekyll build
```
