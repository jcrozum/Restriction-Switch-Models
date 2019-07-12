# Restriction-Switch-Models
Two models of the cell cycle restriction switch: a Hill kinetics version and a mass action kinetics version.

Analysis and simulation of two models of the cell cycle restriction switch from Rozum and Albert 2019 (Submitted to Advances in Complex Systems). See manuscript text for further details on the models.

The three files HRS_MotifX-Funcitonality.ipynb (where X is 1, 2, or 3) are SageMath notebooks that randomly generate parameters and test the stable motifs (as labeled in the manuscript text) for functionality. The output is saved in the nine sobj files. 

CorrelationPlots.ipynb is a SageMath notebook that reads the nine sobj files and generates plots of parameter correlations.

The CRS_Myc-pRB-Control.ipynb file is a Python notebook that uses PySB (https://pysb.readthedocs.io/en/stable/) to simulate a mass action kinetics version of the restriction switch, including the control intervention discussed in the main text. The control simulations used to generate the plots in the manuscript's appendix are implemented in a similar manner in notebooks prefixed with "CRN".

RS_HIll_Control_Tests.ipynb reads in the output from the PySB simulations. It also runs simulations on the HRS model using analogous control interventions. For parameters, it uses the first strongly functionaly parameter set from the sobj files and uses default parameter values for parameters that do not affect stable motif functionality. It then generates plots comparing the CRS and HRS simulations.
