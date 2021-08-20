<p align="center">
  <img  src="https://github.com/swaingotnochill/gsoc-work-report/blob/main/src/gsocxmlpack.png">
</p>

#### Organisation: [mlpack](https://github.com/mlpack)

#### Project: Example Zoo

#### Mentor: [Marcus Edel](https://github.com/zoq) and [Kartik Dutt](https://github.com/kartikdutt18)

## Abstract
This year my proposal `Example Zoo` was selected as part of Google Summer of Code, 2021.`mlpack` is an intuitive, fast and flexible `C++` machine learning library with bindings to other languages. The idea behind the project is to have some readily available code templates and models for newcomers to understand the usage of library and use them in their project. This project will demonstrate the potential of mlpack for real-life examples as well as the Machine Leanring workflow with mlpack.

## Goal
The goal of this proposal was to implement `Linear Regression Model for California Housing Prediciton`, implement `Generative Adversarial Networks for MNIST`,
, implement `Generative Adversarial Networks for Anime Faces(RGB)` and implement `Generative Adversarial Networks for Human Celeb Faces`.

During the course of the project, some blockers were encountered such as very long training time for models, Jupyter Kernel Crashes and Hyperparameter Optimization which consumed a lot of time. 

## Results
We met most of those initially proposed such as mlpack CPP and Python implementation for Linear Regression. Visualization was a big issue in CPP, thus to tackle it, we had to create additonal C Pyton API scripts to make visualization possible in Jupyter Kernel. We also suceeded partially in Generative Adversarial Networks for MNIST, what's remaining is to replace current model with a better trained model. As the training time is too long in mlpack without GPU, we decided to modify the other GAN implementation. We are now translating Pytorch Model into mlpack model. 

## Contributions
Contributions were made to the [mlpack/examples](https://github.com/mlpack/examples).

## mlpack/examples Contributions

<!-- <p align="center">
  <img width="350" height="250" src=".png">
</p> -->

### 1. [Implement Linear Regression for California Housing Price Predictions](https://github.com/mlpack/examples/pull/167)

#### Aim:
1. Add CPP and Python Notebooks.
2. Add EDTA and Visualization using matplotlib and C Python API.
3. Add Metrics for Evaluation.
4. Add markdown documenting the entire flow of the use case.

#### Status :
Merged. Everything in the PR has been completed and merged into the codebase.

### 2. [Implementation of Generative Adversarial Networks for MNIST](https://github.com/mlpack/examples/pull/172)

#### Aim:
1. Add Discriminator Architecture for GAN.
2. Add Generator Architecture for GAN.
3. Add and Train the GAN class model.
4. Load the saved model and generate samples from random noises.
5. Add CPP notebook.
6. Generate images from samples.
7. Optimize and retrain the model based on outputs.
8. Add markdown and comments documenting the entire architecture and flow of the usecase. 

#### Status :
In Review. Everything in the PR has been completed, with very minor changes to be made.

### 3. [Translating Pytorch weights into mlpack for Anime GAN ]()

#### Aim:
1. Add Pytorch Architecutre and translate them into XML.
2. Convert Pytorch weights into CSV.
3. Add mlpack weight converter CPP file.
4. Load model weights and convert them into mlpack serialized weights.
5. Add CPP notebook.
6. Add markdown and comments documenting the entire flow of the usecase.

#### Status :
In Process. Few of the goals are achieved, with weight converter cpp file in progress.

## Other Contributions
[Refactor Tests to use approx_value function](https://github.com/mlpack/mlpack/pull/2901)

## Scope and Future Work
I would like to continue contributing to mlpack's repositories since it alligns well with my personal area of interest as well. Firstly, I would like to finish remaining parts of the project. Secondly, during the project, I found training deep neural networks with large datasets to be extremely time consuming only with CPU. Thus, I would like to focus on GPU integration with mlpack for faster matrix operations.

## Acknowledgement
  I am extremely grateful to my mentors, Marcus Edel and Kartik Dutt for all their constant support and help. They were very helpful in reviewing and helping me whenever I get stuck. Thanks Marcus for handling the long training schedule of the models and Kartik for weight translator. Both of them were always present to help me via Zoom Calls. This would not be possible without their help and guidance.

  I am also thankful to mlpack community for all their reviews help and suggestions. I am also thankful to Marcus and Ryan that helped me in the very first contribution to mlpack. I enjpyed the mlpack virtual meetups.

 I would also like to thank David, my fellow student developer for helping out at every corner throughout this time period. Finally, thanks to Google Open Source and Google Summer of Code, to provide this opportunity.
