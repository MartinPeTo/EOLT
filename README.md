<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100" align="right"/>

#  Final Project Ironhack Data Bootcamp
*Martin Pérez*

*Data Part Time Barcelona May 2019*


## Content
- [Project Description](#project)
- [Dataset](#dataset)
- [Methodology:](#methodology)
    * [EDA](#eda)
    * [Model](#model)
- [Results](#results)
- [Conclusions](#conclusions)

<a name="project"></a>

## Project Description

Statystical analysis of the end of line tests (EOLT) in a production line of a factory. The product is a printer drawer that feeds a paper roll to a industrial production printer.



<a name="dataset"></a>


## Dataset
=======
# EOLT

## Objective
Statystical analysis of the end of line tests (EOLT) in a production line of a factory.
The product is a printer drawer that feeds a paper roll to a industrial production printer.

### Main questions:
The main questions to answer are the following:

  -Which correlations are between the test variables?
  -Can we predict the final test with the data of two motor tests?
  
## Datasets:

The datasets used are from the logs recorded in the EOLT.

There are three different datasets:

RW: From the rewinder test.

TR: From the transport roller test.

BT: The back tension results. From this one we only are interested in the P/F column.

<a name="methodology:"></a>

=======

## Methodology:

First of all an EDA is done to the RW dataset.

Clean datasets to keep only one row per SN. In the case of the RW and TR we want to keep only the PASS results.

Merge all datasets into one by the SN.

<a name="eda"></a>

### EDA

The EDA objective was to analyse the different RW test variables and their correlations.

The TR test was not analysed because it was less relevant (technically) for the final test we want to predict.

<a name="model"></a>

### Model

In the **model selection** process I will take into account:
1.- It is a binaty classification problem
2.- The data is not very large
3.- The target is very unbalanced (13% vs 87%)
4.- Oversampling method applied.

**Model Selection**
1.- Random Forest Classifier
2.- K-Means

<a name="results"></a>

## Results

The final results of the model are:

F1: 0.74

Confusion Matrix: 

(241, 113)

(695, 1619)


<a name="conclusions"></a>


## Conclusions


The conclusion is that **is not possible to predict the back tension test result** based only in the rewinder and transport roller results.
To improve the resuts we should increase the data and look for more related data, maybe other tests.
