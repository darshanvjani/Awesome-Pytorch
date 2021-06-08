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

# LighterModel_v2.3(with GAP) Model 
## Target

-> Add GAP and remove the last BIG kernel.

## Results:

-> Parameters: 6k

-> Best Train Accuracy: 98.65

-> Best Train Accuracy: 97.89

## Analysis:

-> Adding Global Average Pooling reduces accuracy - WRONG

-> **We are comparing a 10.9k model with 6k model. Since we have reduced model capacity, a reduction in performance is expected. ** [LighterModel_v2.3 Model (CODE))](https://github.com/darshanvjani/Awesome-Pytorch/blob/main/EVAI6/Code%20Drill%20Down%20(Model%20Building)/LighterModel_v2_3(with_GAP).ipynb)

# LighterModel_v2.4(Increased Capacity) Model 
## Target

-> Increase model capacity. Add more layers at the end. 

## Results:

-> Parameters: 11.9k

-> Best Train Accuracy: 99.33

-> Best Test Accuracy: 99.04

## Analysis:

-> The model still showing over-fitting, possibly DropOut is not working as expected! Wait yes! We don't know which layer is causing over-fitting. Adding it to a specific layer wasn't a great idea. 

-> Quite Possibly we need to add more capacity, especially at the end. 

-> Closer analysis of MNIST can also reveal that just at RF of 5x5 we start to see patterns forming. 

-> **We can also increase the capacity of the model by adding a layer after GAP!** [LighterModel_v2.3 Model (CODE))](https://github.com/darshanvjani/Awesome-Pytorch/blob/main/EVAI6/Code%20Drill%20Down%20(Model%20Building)/LighterModel_v2_4(Increased_Cap).ipynb)

# LighterModel_v2.5(maxpool correction & proper dropout) Model 
## Target

-> Increase model capacity at the end (add layer after GAP)

-> Perform MaxPooling at RF=5

-> Fix DropOut, add it to each layer
## Results:

-> Parameters: 13.8k

-> Best Train Accuracy: 99.39

-> Best Test Accuracy: 99.41 

## Analysis:

-> Works!

-> But we're not seeing 99.4 or more as often as we'd like. We can further improve it. 

-> The model is not over-fitting at all.

-> **Seeing image samples, we can see that we can add slight rotation.** [LighterModel_v2.5(maxpool correction & proper dropout)(CODE))](https://github.com/darshanvjani/Awesome-Pytorch/blob/main/EVAI6/Code%20Drill%20Down%20(Model%20Building)/LighterModel_v2_5(maxpool_correction_%26_proper_dropout).ipynb)
