The data used for generating the figures in the paper are the four .mat files, 
which correspond to the A-format simulated recordings before being transformed
into B-format recordings (W, X, Y, and Z channels).

The reason why the B-format recordings are not used is that there are a few 
audio files encountering problems when being read due to certain flaws of the 
"audiowrite" function in MATLAB R2021a (might also occur in other versions).

Please use the four folders first if you would like to repeat the experiment
in the paper. If facing problems in reading some audio files, the four .mat
files can be used alternatively. Please follow the equations below for  
transforming the A-format recordings to the B-format recordings in your code.

W = FLU + FRD + BLD + BRU
X = FLU + FRD - BLD - BRU
Y = FLU - FRD + BLD - BRU
Z = FLU - FRD - BLD + BRU

Note that the B-format recordings in the four folders in the same path with 
this readme file are exactly the results of "audiowrite" applied to the above 
equations.