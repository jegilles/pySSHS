# SSH-Python
 Python toolbox for the scale-space histogram segmentation

This toolbox implements the algorithm described in J.Gilles, K.Heal, "A parameterless scale-space approach to find meaningful modes in histograms - Application to image and spectrum segmentation". International Journal of Wavelets, Multiresolution and Information Processing, Vol.12, No.6, 1450044-1--1450044-17, December 2014

ArXiV: https://arxiv.org/abs/1401.2686

Note: this implementation uses sparse matrices for efficient memory storage of the scale-space plane, and uses a discrete Gaussian kernel based on Bessel functions to speed up the computation.

The main function is SSHS_GSS_BoundariesDetect(hist,type) where hist is a 1D array of the histogram to segment and type is method to be used to select the meaningful boundaries. This function calls two functions that can be used independently:
- SSHS_PlanGaussianScaleSpace which computes the scale-space representation of the given histogram
- SSHS_MeaningfulScaleSpace which extract the meaningful minima from a given scale-space representation

The resulting boundaries can be plotted on the histogram by using the function SSHS_PlotBoundaries

Author: Jerome Gilles

Date: 12/13/2024
