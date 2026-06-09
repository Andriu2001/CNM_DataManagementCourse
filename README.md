# README

# Reconstruction
- Supervisor: Consuelo Guardiola Salmeron
- Funding Agency: AEI (Spanish Government)

# Data Organization
- Json file or txt file that has paths to the datasets
- There are two main Datasets (simulations):
  -   Dataset corresponding to Allpix Squared data: located in /home/asanchis/simulaciones/andrea/3D_cylinder/output/
  -   Dataset corresponding to Sentaurus data (2D and 3D simus): located in /home/asanchis/simulaciones/bin/

# How to use the dataset/scripts
## Data corresponding to Allpix simulations:
### Start a simulation
1) Access the container:

asanchis@pc518:~/simulaciones/andrea/3D_cylinder$ apptainer shell \
  --bind ~/allpix-squared:/allpix-squared \
  --bind ~/simulaciones:/data \
  /home/asanchis/allpix-base.sif

2) Execute the simulation using xxx.conf file

Apptainer> /allpix-squared/build/src/exec/allpix -c /data/andrea/3D_cylinder/xxx.conf

### Process data from a simulation
1) Change the directory to the one containing the data:

Apptainer> cd ~/simulaciones/andrea/3D_cylinder/output/

2) Process the data using Propagated_Energy_Spectrum2.ipynb

Apptainer> python3 Propagated_Energy_Spectrum2.ipynb 

## Data corresponding to Sentaurus simulations:

1) Change to the corresponding folder containing the data:
 - 3D simulations:
   Apptainer> cd ~/simulaciones/bin/3D_Sentaurus
 - 2D simulations:
   Apptainer> cd ~/simulaciones/bin/2D_Sentaurus
   
2) Execute the analysis code
 - 3D simulations:
   -   visualize_ElectrostaticPotential.py
   -   visualize_ElectricField.py
   -   sumN_3D_ElectricFields.py
 - 2D simulations:
   -   visualize_2D_Electric_Fields.py
   -   sumN_2D_ElectricFields.py

# LICENSE
- Creative Commons
