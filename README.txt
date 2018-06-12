# Gain-Control-With-IA

This repository includes simulation code used in 

Title: Gain control with A-type potassium current: I_A as a switch between divisive and subtractive inhibition

Authors: Joshua H Goldwyn, Bradley R Slabe, Joseph B Travers, David Terman

Published in: PLoS Computational BiologyThe authors make following code available for scientific research and educational purposes:


**** C CODE ****

ga.c
A single-compartment model with Hodgkin-Huxley-like model of spiking dynamics and A-type Potassium current

gaCable.c
A multi-compartment neuron model with the first compartment representing the soma and spike-generator region and the other 9 compartments representing a dendritic process 

These programs can be compiled with the make file (included)
>> make

and can be run with appropriate inputs as follows

For single-compartment model:

>> ./ga [writeData] [tStop] [ga] [gsyne] [gsyni] [rsyne] [rsyni]

where values are
writeData = 1 to save all variables, 2 to only record spike times
tStop = duration of simulation in milliseconds
ga = A-channel conductance (typically 0-50)
gsyne = excitatory synaptic conductance (typical 0.2-0.7)
gsyni = inhibitory synaptic conductance (typicall 0-2)
rsyne = excitatory synaptic event rate (typically 0-200)
rsyni = inhibitory synaptic event rate (typically 0-70)


For 10-compartment model:

>> ./gaCable [writeData] [tStop] [ga] [gsyne] [gsyni] [rsyne] [rsyni] [d] [synCable]

where values are
writeData = 1 to save all variables, 2 to only record spike times
tStop = duration of simulation in milliseconds
ga = A-channel conductance (typically 0-60)
gsyne = excitatory synaptic conductance (typically 0-5)
gsyni = inhibitory synaptic conductance (typically 1)
rsyne = excitatory synaptic event rate
rsyni = inhibitory synaptic event rate (typically 50)
d = diffusion constant for axial current flow
synCable = compartment number of excitatory inputs


a text data files are created with names like
"data1cpt_xxxx.txt" or "data10cpt_xxxx.txt" [if writeData variable is 1]
"spike1cpt_xxxx.txt" or "spike10cpt_xxxx.txt" [if writeData variable is 2]

To plot voltage as a function of time, for instance
run either code with writeData = 1
The first and second columns of the output data txt file are time and voltage, respectively



**** XPP CODE ****


