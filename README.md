## Supporting repository for the manuscript "Towards generative AI-based fMRI paradigms: reinforcement learning via real-time brain feedback"
#### This repository contains code to reproduce simulations, hyperparameter tuning, plots and contains all the data seen during real-time fMRI acquisition (except nifti files)

### List of Notebooks Containing the code:
1. soft_q_gridsearch: containing the code to reproduce the results of the gridsearch hyperparameter search
2. sim_analysis: plot showing the effects of hyperparameters on the RL learning process
3. single_subject_results: shows mean absolute percentage error (MAPE), convergence, final Q-tables and Q-table steps for each participant and run
4. group_results: shows the average results for all participants
5. group_statistics: Calculation of statistics for all and single subjects with a focus on MAPE
6. run_simulation: code to interactively run the simulation with optimal hyperparameters
7. ground_truth: code to reproduce the frequency ground truth (simulation) and linear contrast scaling of the checkerboard stimuli (real-time fMRI)

### Participants data:
Available in the data folder. Individual participant's data is store in {sub-id}/{run}/log/log.json.

sub-id: e.g. sub-001
run: data_1 (run 1), data_2 (run 2)

### Hyperparameters:
All the hyperparameters used during a participant's run are available in the {sub-id}/{run}/log/setting.conf file

### RL environment (simulation only):
Implemented in the checkerboard_env folder

### RL agent (simulation only):
Implemented in the agents folder

For the real-time fMRI version of the environment and agent, see the main software repository:
https://anonymous.4open.science/r/RLBF-FF35
