
### Installations_of_MadGraph
In this repository explain MadGraph and installation of pakages required to run it and to get Histograms.  
After opening the UBuntu desktop install the updated version of MadGraph by browser. 
Or install by command
"wget https://launchpad.net/mg5amcnlo/3.0/3.5.x/+download/MG5_aMC_v3.5.7.tar.gz 
It is a zip file than open terminal for unzip it.
# Unzip of MadGraph
There is a file like " MG5_aMC_v3.5.7.tar.gz" in our Download file.   
1) Open terminal with (Ctrl+Alt+T)    
2) cd Download  (it open Download file)  
3) tar -xvzf MG5_aMC_v3.5.7.tar.gz   (it is for unzip the zip file. After it will be MG5_aMC_v3_5_7)  
4) cd MG5_aMC_v3_5_7   (open the MadGraph file)  
5) ./bin/mg5_aMC   (launch a MadGraph shell)  
Some pakages are install inside the shell   
6) \>install pythia-pgs (install pythia_pkg)  
7) \>install MadAnalysis  (install MAdAnalysis)
8) \>install pythia8 (install pythia_pkg)
9) \>install LHAPDF6 
10) \>install Delphes
## Some other Pakages are required  
Some other pakages are install outside the MadGraph Shell.  
1) python
2) gfortran


# Installation of python
For installation open the terminal with (Ctrl+Alt+T) and use commands
1) sudo apt update
2) sudo apt install python3.8 python3.8-venv python3.8-dev -y  
Above is enough for python working.  
For set the environment, open Madgraph
3) cd MG5_aMC_v3_5_7
4) python3.8 -m venv mg5env
5) source mg5env/bin/activate

# Installation of gfortran 
For installation of gfortran use commamds  
1) sudo apt-get install gfortran  
2) sudo apt install build-essentials  
## Auto-installation
Some other packages Auto install in MadGraph shell during operating like cuttools, iregi, ninja, collier, py6 etc

######################################### Errorr ####################################################  

If path errorr shows again and again set to fix it by ./bashrc file, open the file by vi command    
1) vi ~/.bashrc  
2) write here "
# === LHAPDF for MG5_aMC_v3_5_10 (Python 3.8) ===
export LHAPDF_ROOT=/home/sanaz/MG5_aMC_v3_5_12/HEPTools/lhapdf6_py3
export PYTHONPATH=$LHAPDF_ROOT/lib/python3.8/site-packages:$LHAPDF_ROOT/lib/python3.8/dist-packages:$PYTHONPATH
export LD_LIBRARY_PATH=$LHAPDF_ROOT/lib:$LD_LIBRARY_PATH
export LHAPDF_DATA_PATH=/home/sanaz/MG5_aMC_v3_5_12/HEPTools/lhapdf6_py3/share/LHAPDF
export PATH=$HOME/MG5_aMC_v3_5_12/HEPTools/cmake/bin:$PATH"
3) escape with :wq  
   
