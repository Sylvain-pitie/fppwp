# fppwp
Friendly Plot Phonon with Phonopy

This python script will allow you to generate plot of phonon in an automatic way.

In order to use it you have to install phonopy:
      https://phonopy.github.io/phonopy/

VASkit:

    https://vaspkit.com/

and Numpy:

      pip3 install numpy

Then dowload the fppwp file and put it in you path.

The command:
      fppwp -h 
will give you this  message:

usage: FPPwP1.0 (Friendly Plot Phonon with Phonopy [-h] [-t TITLE] [-o OUTPUTFILE]

optional arguments:

      -h, --help            show this help message and exit
      -t TITLE, --title TITLE
                        title of the figure, default nothing
      -o OUTPUTFILE, --outputfile OUTPUTFILE
                        name of the output, default tmp.pdf

To use it, you to first make the calculation of the forces for the POSCAR files obtained with phonopy, please use this:

      phonopy -d --dim="X Y Z"  # X,Y and Z are integers
