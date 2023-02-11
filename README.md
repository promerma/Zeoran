# Generate-Zeolite-Frameworks

## Author's information
	Pablo Romero Marimon
	Eindhoven University of Technology
	Department of Applied Physics
	Materials Simulation and Modelling group
	February 10, 2023

## Description
This repository was done as part of my Master's thesis at the MS&M group. Its main goal is to generate multiple .cif files with zeolite structures having different aluminium substitutions. The software is entirely written in C++ and contains a bash script to execute it, which requires the g++ compiler to be installed.

## Content

## Structure of generate.input
The generate.input file needs to have a particular structure. Please, note that he number of parameters and their order cannot be changed. This strcture is as follows:

	Zeolite (MFI/MOR/FAU/RHO/MEL/TON/new)
	Algorithm (chains/clusters/merw/random)
	Name_of_output_directory
	Number_of_structures_to_be_generated
	Extra_parameters

The amount and type of Extra_parameters depend on the algorithm we are using (chains/clusters/merw/random). In each case, these parameters are:

#### chains:

	Number_of_chains
	Number_of_substitutions_in_first_chain
	Number_of_substitutions_in_second_chain
	...
	Number_of_substitutions_in_last_chain

#### clusters:

	Number_of_substitutions
	
#### merw:
	
	Number_of_substitutions
	Number_of_equilibration_steps
	Number_of_visits

NOTE: The last two parameters are optional. If they are missing the default values are 100 and 20 respectively. Note that if changed, both of them need to be specified.

#### random:

	Number_of_substitutions

## How to work with a new zeolite
