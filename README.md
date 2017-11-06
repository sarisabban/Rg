# Rg
A small python script that calculates the Radius of Gyration (Rg) of a protein.

## Description
This is a very small python script with a function that calculates the Radius of Gyration (Rg) of a protein given its .pdb structure file. It is adapted from the [PyMol script](https://pymolwiki.org/index.php/Radius_of_gyration) to become a stand alone function indipendent of PyMol and capable of running on Python 3.

## How To Use
1. The script runs best on single chain protein structures where the file is composed only of ATOM (no heading or anything else), therefore clean up the structure using the following command (capital letters are user specified information):

`grep ATOM FILENAME.pdb | awk '$1 == "ATOM" && $5 == "CHAIN"' > NEW_FILENAME.pdb`

**NOTE**: This command can sometimes chunk up and cut parts of the protein chain (this does not affect the Rg score), but the resultant structure should not be used blindly.

2. Run Rg calculation using the following command:

`python3 Rg.py NEW_FILENAME.pdb`
