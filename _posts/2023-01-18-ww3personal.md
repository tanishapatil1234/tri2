---
toc: true
comments: true
layout: post
title: PocketTherapist Plan ~ Personal Accomplishments
description: Plans/ideation 
type: tangibles
courses: { compsci: {week: 1} }
---

## Sub ticket Tanisha CNN implementation 

### Week 1: Planning and Data Preparation

**Day 0: Sprint Planning**

- [x] - Define the project scope and objectives.
- [x] - Set up a Scrum board or project plan (like this).
- [x] - Kick-off meeting to clarify goals and expectations.

**Day 1: Data Collection**

- [x] Gather a dataset of facial images labeled with emotions ( Kaggle's FER-2013 dataset)
<img width="665" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/aefca214-6f59-4975-a5c9-823496d45cf2">

- [x] Clean the dataset by removing irrelevant or low-quality images.
<img width="656" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/82e74f42-47f2-4699-a612-115199c22c67">


<img width="538" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/442cc8fe-4ad4-489d-b922-6c3ab8c1508b">



**Day 2: Data Preprocessing**

- [x] Resize images to a consistent format (e.g., 224x224 pixels).
> Edit: pre cleaned data set, no need for this!
- [x] Normalize pixel values to a common scale (e.g., [0, 1]).
<img width="302" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/7feeee5f-7b9d-4163-a821-dd545566733e">

- [x] Split the dataset into training, validation, and test sets.
- [x] Augment the training dataset (e.g., rotate, flip, zoom) to increase diversity. ENSURE EQUAL DIST. 

<img width="485" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/2f132c33-474b-4e9d-b1ce-bef77c663d01">

**Day 3: Model Architecture Design**

- [x] Decide on a CNN architecture (e.g., VGG16, ResNet, or custom architecture).
- [x] Define the layers, filters, and activation functions for the model.
<img width="699" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/2d6536c6-3b40-45d7-a1d2-3b170f20ac63">
> Model weights and architecture defined. 

**Day 4: Model Implementation**

- [x] Start coding the CNN model in a deep learning framework like TensorFlow or PyTorch.
- [x] Implement forward and backward passes, loss function, and optimization algorithm (e.g., Adam).
- [x] Ensure the model can handle the input image size and number of classes.

**Day 5: Training**
####(CURRENT)
<img width="699" alt="image" src="https://github.com/vivianknee/PocketTherapist/assets/111611921/6bce9f7e-9584-4c5f-912a-d9799364af4c">

- [x] Train the model on the preprocessed dataset.
- [x] Monitor training metrics such as loss and accuracy.
- [x] Use early stopping if validation performance stalls.
- [x] Document training progress on your Scrum board.

**Day 6: Model Evaluation**

- [x] Evaluate the model's performance using the test set.
- [x] Calculate metrics like accuracy, precision, recall, and F1-score.
- [x] Identify potential sources of bias or error and document them.

### Week 2: Model Optimization and Deployment

**Day 7: Hyperparameter Tuning**

- [x] Fine-tune hyperparameters, like learning rate, batch size, or dropout rates.
- [x] Experiment with different CNN architectures to improve performance.

**Day 8: Error Analysis**

- [x] Analyze model errors on the test set to understand common misclassifications.
- [x] Adjust the model or dataset to address error patterns.

**Day 9: Model Interpretability**

- [x] Implement visualization techniques (e.g., Grad-CAM) to understand what the model focuses on when making predictions.

**Day 10: Model Optimization**

- [x] Implement model optimization techniques (e.g., weight quantization or model pruning) for deployment on resource-constrained devices.

**Day 11: Deployment Setup**

- [x] Set up the infrastructure and environment for model deployment (e.g., cloud server or edge device).
- [x] Create an API or interface for the model.

**Day 12: Testing and Validation**

- [x] Test the deployed model to ensure it functions correctly in the production environment.
- [x] Validate the model's real-world performance.

**Day 13: Documentation and Training**
- [x] Document the model architecture, training process, and deployment steps.
- [x] Train end-users or colleagues on using the model effectively.

**Day 14: Final Review and Retrospective**

- [x] Review the project's achievements and ensure all requirements are met.
- [x] Conduct a retrospective meeting to discuss what went well and what could be improved in the development process.
- [x] Plan for future iterations or improvements.