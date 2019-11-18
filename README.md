# Complex_NMF
This repository is for using NMF and complex NMF. Comments in the codes are written in Japanese.


# Description
Main contents are devided into two types.
1. NMF: just decomposing non negative spectrogram into basis and activation.
2. CNMF: decomposing complex spectrogram with using phase values.

In this context, the basis matrix is considered to be fixed. Therefore, please give them initial basis matrix. Note that the activation is initialized by gaussian distribution.

# Usage
## NMF
First, please prepare the spectrogram whose type is ndarray. Also, prepare the initial values of basis matrix. Note that the number of frequency bins must be the same number between the spectrogram and the initial values.
```
$ python NMF.py [path_to_spectrogram.npy] [iterations] [path_to_initial_values]
```
Arguments:  
1. Path to the spectrogram file made by ndarray.
2. The number of overall iterations.
3. Path to the initial values of basis matrix


Return:
Automatically saved ndarray as ".npy". In addition, automatically draw the learning curve.
1. basis matrix (basis_calc.npy)
2. activation matrix (activation_calc.npy)
3. Errors based on the euclid_divergence (cost.npy)
<div align="center">
<img src="learning_curve_NMF.png" alt="" title="", width="400">
</div>

## Complex NMF
