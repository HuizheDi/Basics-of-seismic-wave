------------------------
Description of functions
------------------------
create_mod.m    - create P-wave velocity model on-the-fly 
	         (requires to set model.MODEL=2 in inp_model.m)

def_acq.m       - manually define acquisition geometry 
		 (requires to set model.ACQ=1 in inp_model.m)

extend_model.m  - extend vp model by PML layers

extract_model.m - extract original vp model and computed pressure wavefield from extended model

germaine.m      - main Matlab code for FDFD

init_A_AC_5p.m  - assemble and use impedance matrix for 5 point FD stencil 
		 (requires to set FD_SCHEME=1 in germaine.m)

init_A_AC_9p_mixed.m - assemble and use impedance matrix for 9 point mixed gridFD stencil with PMLs 
		       (requires to set FD_SCHEME=2 in germaine.m)

inp_model.m    - definition of grid geometry and modelling parameters

PML.m	       - definition of PML damping profiles for 9-point FD mixed grid stencil

read_acq.m     - read acquisition geometry from source and receiver files in folders receiver/ and source/
		 (requires to set model.ACQ=2 in inp_model.m)	

read_mod.m     - read P-wave velocity model from IEEE-le binary files
		 (requires to set model.MODEL=1 in inp_model.m)

RHS_AC.m       - assemble source vector RHS

shift_acq.m    - shift discrete acquisition geometry by model.npml in x- and y-direction
