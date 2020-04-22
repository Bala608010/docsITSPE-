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
1. directory_config : Managing the Directorys
   - Input_directory : The directory which contains the model.
   - temp_directory : The directory to which the temporary files should be created. 
2. File_requried : Managing the file needed to run sumo
   - network_file : network file to to sumo model 
   - sumo_config_file : configuartion file for sumo
   - routes_file : Routes file for sumo model 
   - Undated_tlLoggic_file : The initial TlLogiic for the model from the network file. 
   - additional_taz_file : Traffic assignement zones file
   - additional_vehicle_type_file : Additional file containing the vehicle type. 
   - additional_e_file : Additional Detector file.
   - end_time : The time upto which sumo has to run.
3. PSO_configuration : Managing the PSO parameters. 
   - Iterations : Number of iterations for PSO. 
   - no_of_particles : Number of particles for PSO.
   - options : dict with keys {'c1', 'c2', 'w', 'p', 'k'} – a dictionary containing the parameters for the specific optimization technique
     - c1 (float): cognitive parameter
     - c2 (float): social parameter
     - w (float): inertia parameter
     - p (int {1,2}) : the Minkowski p-norm to use. 1 is the sum-of-absolute values (or L1 distance) while 2 is the Euclidean (or L2) distance.
     - k (int): number of neighbors to be considered. Must be a positive integer less than n_particles. 
    - multiplier_number : The upper limit ot the value that each element in the each particle can take for initial guess. 
    - percentage : the percentage of particles near the input particle. 
4. Objective_function : Manage the parameters for Objective function. 
   - cost_function_type : we can choose how to calculate the cost function. 
     - diff : Just take the difference between actual flow and the simulated flow. 
     - MAPE : Mean Absolute Percentage Error of the actual flow and the simulated flow.
     - GEH : GEH Statistic of the actual flow and the simulated flow.
   - attribute_eoutput : The attribute to be considered for calculating the cost from the e_output files. 
   - type : There are two modes of running the file. 
     - online : We will be runing Dusrouter for the model
     - offline : We will be runing sumo for the model


## References 
SUMO 
    - https://sumo.dlr.de/docs/

PSO 
    - https://www.youtube.com/watch?v=JhgDMAm-imI 
    - https://en.wikipedia.org/wiki/Particle_swarm_optimization

MAPE 
    - https://www.statisticshowto.com/mean-absolute-percentage-error-mape/

GEH 
    - https://en.wikipedia.org/wiki/GEH_statistic



