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

```bash
conda install -c pytorch pytorch
```

If you want to add the channel to your configuration in a persistent state, use a command such as:

```bash
conda config --append channels pytorch
```

Observant readers will note that this is part of the recommended ACSE anaconda software install process.

If the package is not available in any conda channels, you could install it using pip. Search for the
package you want on [pypi.org](https://pypi.org/). Using the same example of pytorch, if it were not
available through conda channels you might refer to the [pypi torch page](https://pypi.org/project/torch/)
(note the different naming on pypi; there is [redirect from pytorch](https://pypi.org/project/pytorch/))
and install it with:

```bash
pip install torch
```

## Windows Subsystem for Linux

### Can I get a graphical interface to my WSL instance?

Connecting graphically to the WSL instance requires some work but should be straightforward for an experienced Linux user, and a valuable learning process for a Linux beginner. You are aiming to set up a remote desktop connection to WSL, the Windows end of which should be the same as connecting to an Azure Labs VM or other remote system, except that the connection is all local.

Assuming you're using Ubuntu as your WSL instance (methods should be similar for other Linux distributions, but package names and configuration file locations may differ - please submit a PR to update this FAQ if you have documented the process for another distribution!) you need to get a clean install of xdrp (the RDP server) and install a graphical desktop environment (I'll use xfce4 as a lightweight example, but you may prefer a heavier example such as Gnome).

To clean and then install the required (and other useful) packages, run:

```bash
sudo apt-get install xrdp
sudo apt-get install xfce4
sudo apt-get install xfce4-goodies
```

You now need to change the xrdp port to avoid clashes with Windows services, and configure the colour depth, using:

```bash
sudo cp /etc/xrdp/xrdp.ini /etc/xrdp/xrdp.ini.bak
sudo sed -i 's/3389/3390/g' /etc/xrdp/xrdp.ini
sudo sed -i 's/max_bpp=32/#max_bpp=32\nmax_bpp=128/g' /etc/xrdp/xrdp.ini
sudo sed -i 's/xserverbpp=24/#xserverbpp=24\nxserverbpp=128/g' /etc/xrdp/xrdp.ini
```

Enable xfce4 as your default session with:

```bash
echo xfce4-session > ~/.xsession
```

Now you need to edit the xdrp startup file, suggested to use nano with:

```bash
sudo nano /etc/xrdp/startwm.sh
```

Find the following lines and add comments at the beginning (they will by default be uncommented):

```bash
#test -x /etc/X11/Xsession && exec /etc/X11/Xsession
#exec /bin/sh /etc/X11/Xsession
```

Add the following new lines:

```bash
# xfce
startxfce4
```

Now start xdrp with:

```bash
sudo /etc/init.d/xrdp start
```

You can now run the Remote Desktop Connection app on Windows, connecting to localhost:3390 and authenticating with the username and password you supplied when you installed your WSL Linux instance.

## Docker

### I've installed Docker; now what do I do?

Try starting out with the [Docker 101 tutorial](https://www.docker.com/101-tutorial).
