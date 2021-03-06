# Installation

Installing {{autodiff}} is easy, since it is a *header-only library*. Follow
the steps below.

## Installation using Conda

If you have [Anaconda] or [Miniconda] installed (with Python 3.7+), you can
install {{autodiff}} with a single command:

~~~
conda install conda-forge::autodiff
~~~

This will install {{autodiff}} in the conda environment that is active at the
moment (e.g., the default conda environment is named `base`).

## Installation using CMake

If you have `cmake` installed in your system, you can then not only install
{{autodiff}} but also build its examples and tests. First, you'll need to
download it by either git cloning its [GitHub repository][github]:

~~~
git clone https://github.com/autodiff/autodiff
~~~

or by [clicking here][zip] to start the download of a zip file, which you
should extract to a directory of your choice.

Then, execute the following steps (assuming you are in the root of the source code directory of {{autodiff}}!):

~~~
mkdir .build && cd .build
cmake ..
cmake --build . --target install
~~~

!!! attention

    We assume above that you are in the root of the source code directory, under
    `autodiff`! The build directory will be created at `autodiff/.build`.
    We use `.build` here instead of the more usual `build` because there is a
    file called `BUILD` that provides support to [Bazel](https://bazel.build/) build system.
    In operating systems that treats file and directory names as case insensitive,
    you may not be able to create a `build` directory.

The previous installation commands will require administrative rights in most
systems. To install {{autodiff}} locally, use:

~~~
cmake .. -DCMAKE_INSTALL_PREFIX=/some/local/dir
~~~

## Installation by copying

Assuming the git cloned repository or the extracted source code resides in a
directory named `autodiff`, you can now copy the sub-directory
`autodiff/autodiff` to somewhere in your project directory and directly use
{{autodiff}}.


## Installation failed. What do I do?

Discuss with us first your issue on our [Gitter Community Channel][gitter]. We
may be able to respond more quickly there on how to sort out your issue. If bug
fixes are indeed required, we'll kindly ask you to create a [GitHub
issue][issues], in which you can provide more details about the issue and keep
track of our progress on fixing it. You are also welcome to recommend us
installation improvements in the Gitter channel.



[Anaconda]: https://www.anaconda.com/distribution/
[Miniconda]: https://docs.conda.io/en/latest/miniconda.html
[gitter]: https://gitter.im/autodiff/community
[github]: https://github.com/autodiff/autodiff
[zip]: https://github.com/autodiff/autodiff/archive/master.zip
[issues]: https://github.com/autodiff/autodiff/issues/new
