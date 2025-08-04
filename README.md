# MTP-SiC-Cs
This repository contains a fitted moment tensor potential (SiCCs.mtp) developed for the amorphous SiC-Cs system. The potential enables accurate and efficient atomic simulations to study Cs diffusion in amorphous SiC.

## Use guide
### Software requirements
1. LAMMPS https://github.com/lammps/lammps.git
2. Moment tensor potential (MTP) development https://gitlab.com/ashapeev/mlip-2
### Use of the developed MTP
1. Please make sure you have already install a MLIP plugin into LAMMPS; otherwise see https://gitlab.com/ashapeev/interface-lammps-mlip-2
2. Add the following content in the LAMMPS input script to define the potential:  
   pair_style mlip mlip.ini  
pair_coeff * *  
Detailed useage tutorial of MTP can be found at https://gitlab.com/ashapeev/mlip-2-tutorials
3. Please define the atomic id of elements in the structural file in the following order: 1-C; 2-Si; 3-Cs

## Citation
If you utilize the potential in this repository, please cite: 
