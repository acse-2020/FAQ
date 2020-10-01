# FAQs regarding software for the ACSE course

Software installs for ACSE students are [documented in detail here](https://acse-2020.github.io/introduction/software/intro.html).
Questions relating to errors or significant omissions in that file can be raised as questions
here but are likely to be resolved as bug-fixes on the software intro page.

This FAQ is primarily for questions relating to installs on non-standard platforms, background 
detail on the software installs, corner-case errors, and questions relating to the post-installenvi
ronment.

## Anaconda

### I want to install an additional package, but it's not available as a conda install

You have a couple of options. Firstly, there are a number of additional Anaconda channels which may
contain the package you're looking for. Try searching on [Anaconda Cloud](https://anaconda.org/) and
if you need to install from a different channel, use the supplied command. For example, if you wanted
to install the [pytorch package](https://anaconda.org/pytorch/pytorch) you would use:

```
conda install -c pytorch pytorch
```

If you want to add the channel to your configuration in a persistent state, use a command such as:

```
conda config --append channels pytorch
```

Observant readers will note that this is part of the recommended ACSE anaconda software install process.

If the package is not available in any conda channels, you could install it using pip. Search for the 
package you want on [pypi.org](https://pypi.org/). Using the same example of pytorch, if it were not
available through conda channels you might refer to the [pypi torch page](https://pypi.org/project/torch/) 
(note the different naming on pypi; there is [redirect from pytorch](https://pypi.org/project/pytorch/))
and install it with:

```
pip install torch
```
