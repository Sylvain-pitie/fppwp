# fppwp
Friendly Plot Phonon with Phonopy

This python script will allow you to generate plot of phonon in an automatic way.

In order to use it you have to install phonopy:
      https://phonopy.github.io/phonopy/

VASPkit:

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
      for f in POSCAR-*
      do
      mkdir "force-"$f
      cd "force-"$f
      cp ../POTCAR .
      cp ../$f POSCAR
      cp ../KPOINTS .  #here the appropriate kpoint file
      cp ../INCAR .    #here the appropriate INCAR file
      cd ../
      done

When the vasp calculations are done, you can use the fppwp script and you will obtain the tmp.pdf file.
If you want to add title and change the ouptut here is an exemple:

            fppwp -t 'I use fppwp' -o friendly_phonon.pdf

Enjoy! :D
      
