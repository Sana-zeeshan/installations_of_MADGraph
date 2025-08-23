
### Installations_of_MadGraph
In this repository explain MadGraph and installation of pakages required to run it and to get Histograms.  
After opening the UBuntu desktop install the updated version of MadGraph by browser. It is a zip file than open terminal for unzip it.
# Unzip of MadGraph
There is a file like " MG5_aMC_v3.5.7.tar.gz" in our Download file.   
1) Open terminal with (Ctrl+Alt+T)    
2) cd Download  (it open Download file)  
3) tar -xvzf MG5_aMC_v3.5.7.tar.gz   (it is for unzip the zip file. After it will be MG5_aMC_v3_5_7)  
4) cd MG5_aMC_v3_5_7   (open the MadGraph file)  
5) ./MG5_aMC   (launch a MadGraph shell)  
Some pakages are install inside the shell   
6) \>install pythia-pgs (install pythia_pkg)  
7) \>install MadAnalysis  (install MAdAnalysis)  

## Some other Pakages are required  
Some other pakages are install outside the MadGraph Shell.  
1) python
2) LHAPDF
3) gfortran

# Installation of python
For installation open the terminal with (Ctrl+Alt+T) and use commands
1) sudo apt update
2) sudo apt install python3.8 python3.8-venv python3.8-dev -y  
Above is enough for python working.  
For set the environment, open Madgraph
3) cd MG5_aMC_v3_5_7
4) python3.8 -m venv mg5env
5) source mg5env/bin/activate

# Installation and Set Environment of LHAPDF
First open Ubuntu desktop and install LHAPDF by browser and unzip it by following commands  
1) Open terminal with (Ctrl+Alt+T)  
2) cd Download  (it open Download file)
3) tar -xvzf LHAPDF-6.5.5.tar.gz   (it is for unzip the zip file. After it will be LHAPDF-6.5.5 )  
4) cd LHAPDF-6.5.5   (open the LHAPDF file)
5) #https://lhapdf.hepforge.org/install.html
it required " sudo apt install autoconf" command
6) autoreconf -f -i
7) ./configure --prefix=$PWD/../lhapdf_inst
8) make
For set environment of LHAPDF, go to directory cd MG5-aMC/HEPTools/lhapdfpy3/lib   
9)export PATH=$PWD/lhapdf_inst/bin:$PATH
10)export PDFSETS_PATH=$PWD/lhapdf_inst/share/LHAPDF:$PDFSETS_PATH
11)export LD_LIBRARY_PATH=$PWD/lhapdf_inst/lib:$LD_LIBRARY_PATH
12)export PYTHONPATH=$PWD/lhapdf_inst/lib64/python2.6/site-packages:$PYTHONPATH

# Installation of gfortran 
For installation of gfortran use commamds
1) sudo apt-get install gfortran
2) sudo apt install build-essentials
## Auto-installation
Some other packages Auto install in MadGraph shell during operating like cuttools, iregi, ninja, collier, py6 etc
