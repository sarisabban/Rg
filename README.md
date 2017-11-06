# Rg
A small python script that calculates the Radius of Gyration (Rg) of a protein.

## Description
This is a very small python script with a function that calculates the Radius of Gyration (Rg) of a protein given its .pdb structure file. It is adapted from the [PyMol script](https://pymolwiki.org/index.php/Radius_of_gyration) to become a stand alone function indipendent of PyMol and capable of running on Python 3.

## How To Use
1. The script runs best on single chain protein structures where the file is composed only of ATOM (no heading or anything else), therefore clean up the structure using the following command:

`grep ATOM FILENAME.pdb > NEW_FILENAME.pdb`

Capital letters are user specified information

2. Run using the following command:

`python3 Rg.py NEW_FILENAME.pdb`
