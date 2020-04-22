# docsITSPE
# Optimizing ODE
To optimize OD_matrix we are using Particle Swarm Optimizer(PSO). 

For the implemtaion of the PSO we chose a PSO toolkit called Pyswarms 

# Prerequisite 
1. Sumo Version 1.5.0
2. Python3
3. Pyswarms 
    For installations and information about Pyswarms please refer - https://pyswarms.readthedocs.io/en/latest/

For optimzing the OD_matrix we requrie three files: 
1. PSO_code.py - PSO code
2. fun_req.py - Functions that are requried to run the PSO_code.py file
3. config.ini - Configuration file to configure variables in the code

The following attributes/elements are used within config.ini:
1. directory_config - Managing the Directorys
   a. Input_directory - The directory which contains the model.
   b. temp_directory - The directory to which the temporary files should be created.
   c. 
    




