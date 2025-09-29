# MTP-SiC-Cs
This repository contains fitted moment tensor potentials developed for the amorphous SiC-Cs system and polycrystalline SiC-Cs system. The potentials enable accurate and efficient atomic simulations to study Cs diffusion in amorphous SiC and polycrystalline SiC with high energy grain boundaries.

## Use guide
### Software requirements
1. LAMMPS https://github.com/lammps/lammps.git
2. MLIP-2 package https://gitlab.com/ashapeev/mlip-2
3. MLIP-3 package https://gitlab.com/ashapeev/mlip-3
### Use of the developed MTP
There are three fitted MTPs in the Potential folder: aSiC.mtp, HEGB_L10.almtp, HEGB_L16.almtp <br>
* aSiC.mtp: level 16 MTP, specialized for amorphous SiC-Cs system <br>
* HEGB_L10.almtp: level 10 MTP, faster, specialized for polycrystalline SiC-Cs system <br>
* HEGB_L16.almtp: level 16 MTP, more accurate, specialized for polycrystalline SiC-Cs system <br>
1. If you want to use aSiC.mtp, please make sure you have already installed the MLIP-2-LAMMPS interface, otherwise see https://gitlab.com/ashapeev/interface-lammps-mlip-2. Add the following content in the LAMMPS input script to define the potential: <br>
pair_style mlip mlip.ini  
pair_coeff * * <br> 
Detailed useage tutorial of MTP can be found at https://gitlab.com/ashapeev/mlip-2-tutorials <br>
2. If you want to use HEGB_L10.almtp or HEGB_L16.almtp, please make sure you have already installed the MLIP-3-LAMMPS interface, otherwise see https://gitlab.com/ivannovikov/interface-lammps-mlip-3/. Add the following content in the LAMMPS input script to define the potential: <br>
pair_style mlip load_from=HEGB_L10.almtp (or HEGB_L16.almtp) 
pair_coeff * * <br>
3. Please define the element types in the structural file in the following order: 1-C; 2-Si; 3-Cs

## Training set
We also provide the training set in the Trainingset folder.

## Computational models
We also provide the models used in this work. Please find them in the Models folder.

## Citation
If you utilize the potentials, training set or models in this repository, please cite: 
