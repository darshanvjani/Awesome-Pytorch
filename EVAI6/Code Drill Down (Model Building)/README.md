# Skelaton Model Base
## Target
-> Get the set-up right

-> Set Transforms

-> Set Data Loader

-> Set Basic Working Code

-> Set Basic Training  & Test Loop

## Results:

-> Parameters: 6.3M

-> Best Training Accuracy: 99.99

-> Best Test Accuracy: 99.24

## Analysis:

-> Extremely Heavy Model for such a problem

-> Model is over-fitting, but we are changing our model in the next step [Skelaton Model Base (CODE))](https://github.com/darshanvjani/Awesome-Pytorch/blob/main/EVAI6/Code%20Drill%20Down%20(Model%20Building)/Skeleton_Model.ipynb)

# Skelaton_v1.0 Model 
## Target

-> Get the basic skeleton right. We will try and avoid changing this skeleton as much as possible. 

-> No fancy stuff

## Results:

-> Parameters: 194k

-> Best Train Accuracy: 99.35

-> Best Test Accuracy: 99.02

## Analysis:

-> The model is still large, but working. 

-> **We see some over-fitting** [Skelaton_v1.0 Model (CODE))](https://github.com/darshanvjani/Awesome-Pytorch/blob/main/EVAI6/Code%20Drill%20Down%20(Model%20Building)/Skeleton_Model_v1_0.ipynb)

# LighterModel_v2.0 Model 
## Target

-> Make the model lighter

## Results:

-> Parameters: 10.7k

-> Best Train Accuracy: 98.85

-> Best Test Accuracy: 98.75

## Analysis:

-> Good model! 

-> **No over-fitting, model is capable if pushed further** [LighterModel_v2.0 Model (CODE))](https://github.com/darshanvjani/Awesome-Pytorch/blob/main/EVAI6/Code%20Drill%20Down%20(Model%20Building)/LighterModel_v2_0.ipynb)

# LighterModel_v2.1(with batchnorm) Model 
## Target

-> Add Batch-norm to increase model efficiency.

## Results:

-> Parameters: 10.9k

-> Best Train Accuracy: 99.9

-> Best Test Accuracy: 99.29

## Analysis:

-> We have started to see some over-fitting now. 

-> **Even if the model is pushed further, it won't be able to get to 99.4** [LighterModel_v2.1 Model (CODE))](https://github.com/darshanvjani/Awesome-Pytorch/blob/main/EVAI6/Code%20Drill%20Down%20(Model%20Building)/LighterModel_v2_1(with_batchnorm).ipynb)

# LighterModel_v2.2(with reg) Model 
## Target

-> Add Regularization, Dropout while keeping batchnorm

## Results:

-> Parameters: 10.9k

-> Best Train Accuracy: 99.41 (20th Epoch)

-> Best Train Accuracy: 99.30

## Analysis:

-> Regularization working. 

-> But with the current capacity, not possible to push it further. 

-> **We are also not using GAP, but depending on a BIG sized kernel** [LighterModel_v2.2 Model (CODE))](https://github.com/darshanvjani/Awesome-Pytorch/blob/main/EVAI6/Code%20Drill%20Down%20(Model%20Building)/LighterModel_v2_2(with_reg).ipynb)
