#GalaxyFill: A program for filling up the missing part of protein structure

##0. Remark
The GalaxyFill distribution version supports only **Linux 64-bit** OS and binary files compiled with serial option.
**Linux 32-bit** OS or binary files compiled with MPI option are not supported.

##1. Installation
1. Download the GalaxyFill program
 * Download a copy of GalaxyFill
    * https://github.com/seoklab/GalaxyFill
    * https://github.com/seoklab/GalaxyFill/archive/master.zip
 * Or, clone the GalaxyFill git repository 
     * git clone https://github.com/seoklab/GalaxyFill.git

2. Unzip and place the downloaded files
 * unzip GalaxyFill.zip
 * mv GalaxyFill $GALAXY_HOME  
    (*example*: GALAXY_HOME=/applic/GalaxyFill)

3. Check the downloaded files
 * There should exist:
  * bin: directory for executables  
    There should be build_initial_model and **GalaxyFill**
  * data: directory for data files
  * examples: directory for example files

4. Set environment variable
 * export GALAXY_HOME=$GALAXY_HOME  
    (*example*: export GALAXY_HOME=/applic/GalaxyFill)

##2. How to use GalaxyFill
1. Prepare the input protein structure in PDB format
 * You have to provide a protein structure in the PDB file format for structure refinement.
 Gaps (or chain breaks) are highly prohibited in the middle of the initial protein structure.

2. Run GalaxyFill
 * Usage: $GALAXY_HOME/bin/GalaxyFill [-h] [-p INPUT PDB File] [-s INPUT FASTA File]
 * Input arguments and options:     
    *  -p or --pdb      : Input protein structure file in PDB format (**mendatory**)    
    *  -s or --seq      : Input protein sequence file in FASTA format (**mendatory**)    
    *  -o or --out      : Output protein structure file name (optional, default=${Input PDB prefix}_fill.pdb)
    *  -t or --title    : Running title for GalaxyFill (optional, default=${Input PDB prefix})

3. Output of GalaxyFill
 * The final refined model will be **${Input PDB prefix}_fll.pdb** or designated by "-o/--out" option

##3. Release log
* 10 Apr 2016: Local energy optimization on the filled residues
* 09 Apr 2016: Added optional arguments: -o and -t
* 01 Feb 2016: The first release of GalaxyFill

##4. References
* E. A. Coutsias, C. Seok, M. P. Jacobson, and K. A. Dill, A Kinematic View of Loop Closure, J. Comput. Chem. 25, 510-528 (2004).

##5. Contact
* chaok@snu.ac.kr
* compbio.galaxy@gmail.com

