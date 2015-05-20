# Getting and Cleaning Data Course Project
## Introduction

This repo contains the Cousera's course *"Getting and Cleaning Data"* project. The goal of this project was to prepare tidy data that can be used for later analysis. 

## Data set
The original data was a selected set of variables from the Human Activity Recognition Using Smartphones.
Then from the original data consistend vairous statistics (see below), a subset of means and standard deviations were selected.

* mean(): Mean value
* std(): Standard deviation
* mad(): Median absolute deviation 
* max(): Largest value in array
* min(): Smallest value in array
* sma(): Signal magnitude area
* energy(): Energy measure. Sum of the squares divided by the number of values. 
* iqr(): Interquartile range 
* entropy(): Signal entropy
* arCoeff(): Autorregresion coefficients with Burg order equal to 4
* correlation(): correlation coefficient between two signals
* maxInds(): index of the frequency component with largest magnitude
* meanFreq(): Weighted average of the frequency components to obtain a mean frequency
* skewness(): skewness of the frequency domain signal 
* kurtosis(): kurtosis of the frequency domain signal 
* bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.
* angle(): Angle between to vectors.



The script containing all R commands is called run_analsyis.R which does the following:
* Accesses https:// and downloads zip file
* Unzips that file
* Reads data
* Does transformations
* Writes tide data sets containing means and standard deviations into .txt file

*The CodeBook.md* explains it in greater details. 

