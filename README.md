![GitHub Logo](https://s3.ap-south-1.amazonaws.com/greyatom-social/GreyAtom-logo.png)

# Tech Basics - Assignment 4

### Install Anaconda

#### Installing 

* Now you already have an executable Anaconda bash script downloaded in [previous assignment](https://github.com/commit-live-students/fsdse-techbasics-assignment-2/). To install now we can run the script:
```
./Anaconda2-4.3.1-Linux-x86_64.sh
```
* You’ll receive the following output:
```
output

Welcome to Anaconda2 2-4.3 (by Continuum Analytics, Inc.)

In order to continue the installation process, please review the license
agreement.
Please, press ENTER to continue
```
* Press ENTER to continue and then press ENTER to read through the license. Once you’re done reading the license, you’ll be prompted to approve the license terms:
```
output

Do you approve the license terms? [yes|no]
```
* As long as you agree, type `yes`. At this point, you’ll be prompted to choose the location of the installation. You can press ENTER to accept the default location, or specify a different location to modify it
```
output

Anaconda2 will now be installed into this location:
/home/username/anaconda2

  - Press ENTER to confirm the location
  - Press CTRL-C to abort the installation
  - Or specify a different location below

[/home/username/anaconda2] >>>

```
* The installation process will continue, it may take some time. Once it’s complete you’ll receive the following output:
```
Output
...
installation finished.
Do you wish the installer to prepend the Anaconda2 install location
to PATH in your /home/username/.bashrc ? [yes|no]
[no] >>>
```
* Type `yes` so that you can use the `conda` command. You’ll next see the following output:
```
Output

Prepending PATH=/home/username/anaconda2/bin to PATH in /home/username/.bashrc
A backup will be made to: /home/username/.bashrc-anaconda2.bak
...

```
* You can also say `No` and can manually add Anaconda path to `.bashrc` file from command line. Open your terminal and type below command
```
export PATH=$PATH:"/home/username/anaconda2/bin"
```
* This will add Anaconda path to `.bashrc` file. You can also do it by editing `.bashrc` file using `nano` command and add path.
* In order to activate the installation, you should source the `~/.bashrc` file:
```
source ~/.bashrc
```
* Once you have done, you can verify your install by making use of the `conda` command, for example with list:
```
conda list
```
* You’ll receive output of all the packages you have available through the Anaconda installation:
```
Output
# packages in environment at /home/username/anaconda2:
#
_license                  1.1                      py35_1  
_nb_ext_conf              0.3.0                    py35_0  
alabaster                 0.7.9                    py35_0  
...
```

#### Updating

* You should regularly ensure that Anaconda is up-to-date so that you are working with all the latest package releases.To do this, you should first update the `conda` utility:
```
conda update conda
```
* When prompted to do so, type `y` to proceed with the update.Once the update of `conda` is complete, you can update the Anaconda distribution:
```
conda update anaconda
```
* Again when prompted to do so, type `y` to proceed.This will ensure that you are using the latest releases of conda and Anaconda.

#### Uninstalling

* If you are no longer using Anaconda and find that you need to uninstall it, you should start with the anaconda-clean module which will remove configuration files when you uninstall Anaconda.
```
conda install anaconda-clean
```
* Type `y` when prompted to do so.
* Once it is installed, you can run the following command. You will be prompted to answer `y` before deleting each one. If you would prefer not to be prompted, add `--yes` to the end of your command:
```
anaconda-clean
```
* This will also create a backup folder called `.anaconda_backup` in your home directory:
```
Output
Backup directory: /home/username/.anaconda_backup/2017-04-25T191831
```
* You can now remove your entire Anaconda directory by entering the following command:
```
rm -rf ~/anaconda2
```
* Finally, you can remove the PATH line from your `.bashrc` file that Anaconda added. To do so, first open nano:
```
nano ~/.bashrc
```
* Then scroll down to the end of the file (if this is a recent install) or type `CTRL + W` to search for Anaconda. Delete or comment out the following lines:
```
# added by Anaconda2 2-4.3 installer
export PATH="/home/username/anaconda2/bin:$PATH"
```
* When you’re done editing the file, type `CTRL + X` to exit and `y` to save changes.Anaconda is now removed.
