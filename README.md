# BayesianSVM.jl
This repository contains the Julia package for the Bayesian SVM algorithm described in the paper [_"Bayesian Nonlinear Support Vector Machines for Big Data"_](https://arxiv.org/abs/1707.05532) by Florian Wenzel, Théo Galy-Fajou, Matthäus Deutsch and Marius Kloft

## Requirements
The BayesianSVM only works for version of Julia > 0.5.
Other necessary packages will automatically be added in the installation

## Installation
To install the last version of the package in Julia run
```
Pkg.clone("git://github.com/theogf/BayesianSVM.jl.git")
```

## Running the Algorithm
A more complete documentation will be created very soon. For now here are the basic steps for using the algorithm :
```
using BayesianSVM
Model = BSVM(X_training,y_training)
Model.Train()
y_predic = sign(Model.Predict(X_test))
y_uncertaintypredic = Model.PredictProb(X_test)
```
Where X_training should be a matrix of size NSamples x NFeatures, and y_training should be a vector of 1 and -1
