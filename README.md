# Purpose

This repo is for code used in:

Leithe S, Møller B, Aagnes B, Nilssen Y, Lambert PC, Myklebust TÅ. Maximal Local Privacy Loss-A New Method for Privacy Evaluation of Synthetic Datasets. Stat Med. 2026;45(1-2):e70376. <https://doi.org/10.1002/sim.70376>

Corresponding author:  Sigrid Leithe sigrid.leithe@fhi.no

# Description

## Introduction
The project is used to generate synthetic time-to-event data and evaluate privacy in terms om *maximum local privacy loss*. Utility metrics and similarity based privacy metrics are also calculated. 

## Organisation of project

[master.do](/stata/master.do)

### Command files are organised depending on their purpose: 

* data preparation [/stata/dataprep](/stata/dataprep)
* synthetic data generation [/stata/generation](/stata/generation)
* evaluation of *maximum local privacy loss* [/stata/maximum_local_privacy_loss](/stata/maximum_local_privacy_loss)
* calculation of utility metrics [/stata/utility](/stata/utility)
* calculation of XGBoost disctrimination propensity score, inference attacks, and similarity based privacy metrics [/python](/python)

### Result files

[/results](/results)

## Parallel computing of generation and risk evaluation

The code *split-apply-combine* **on the local machine** by starting one Stata sessions per group. Starting
a new Stata session is restricted to avoid exhausting computer resources. 

see e.g. [generate.do](/stata/generation/generate.do)
