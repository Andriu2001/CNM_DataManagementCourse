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
## Data corresponding to Sentaurus simulations:

# LICENSE
- Creative Commons
