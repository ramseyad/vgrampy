# vgrampy

### Author: Noel Lefevre (Adapted from Steven Ramsey's LDNH README.md)
### Date: January 29, 2024

Python tools for analyzing electrochemistry voltammograms. The script
`vg2signal.py` processes a potentiostat voltammogram data file using a method
analogous to LDNH, into a signal value and optionally plots the "detilted"
voltammogram. It can also optionally re-center the analysis window on the
empirical peak voltage from the first phase of analysis of the data (which is
_only_ a good idea to run on a voltammogram that has a clear and unambiguous
analyte peak).

# Prerequisites for using this software

- Python 3.9 (it doesn't yet work on Python 3.11)
- `git`
- Coding Application/IDE
- A github account

So far, this software has only been tested on Windows11/x86_64. It has 
not been tested on MacOS 12.6.5 on Apple M1, Linux/x86_64, etc.

# How to install and run `groupvg2.py` for `user-friendly` branch:

1. Download Python 3.9 (can be 3.9.0-3.9.12)
   1. make sure to select `Add Python 3.9 to PATH` when you install it


2. Download a coding application/IDE (i.e. VisualStudio, VSCode, PyCharm)


3. Clone the software repo (2 ways)
   1. sign into your github through the IDE
   2. paste the repo address: `https://github.com/ramseylab/vgrampy.git`


4. Change to the correct branch- for running for one experiment use `user-friendly`
   1. for VisualStudio- on the right side click `Git Changes` and change the drop-down menu


5. Open the command prompt and change your directory to the software repo `cd grampy`
   1. if you open the command prompt within your IDE, it should already be in the right directory


6. Install all of the required packages:
```dockerignore
pip install numpy
```
- depending on your computer, it may be `pip` or `pip3`
- most packages will be install when creating the virtual environment

7. Run the program by typing in 
```
python groupvg2.py
```
- depending on your computer, it may be `python` or `python3` or `py`

# Options for `groupvg2.py`:

- Vwidth

# Troubleshooting:

### Problem: When I try to switch my branch to user-friendly I get the error: 

```
Exception of type 'Microsoft.TeamFoundation.Git.Contracts.GitCheckoutConflictException' was thrown`"
```
This means that the destination branch has more exclusions in .gitignore than the original branch.

**Solution:** in the Git changes, 'ignore' the .suo (or .wsuo) file and then do a force checkout to get to your desired branch.


### Problem: When I am installing the packages, I get an error with `scikit-fda`

This means that you are not using Python 3.9

**Solution:** 
- Uninstall the Python version you have on your computer (make sure it is no longer in PATH). 
- Install Python 3.9 and change your interpreter to the correct version


### Problem: I cannot access the vgrampy github

You need to be added by an admin in order to access the code (currently Noel)

**Solution:** email the admin to get your github account added to the repo