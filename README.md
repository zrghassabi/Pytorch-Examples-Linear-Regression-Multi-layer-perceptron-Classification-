# python_pytorch_pycharm examples
Based on Tutorial https://towardsdatascience.com/understanding-pytorch-with-an-example-a-step-by-step-tutorial-81fc5f8c4e8e


Example1= Linear Regression using Numpy (run on CPU) and Matplotlib

Example2= Linear Regression using Tensors (run on GPU)

Example 3= Linear Regression using nn.sequential model using torch.nn.linear(1,1) (pytorch linear model, no need to define parameters a and b in y=a+b*x)

Example 4= Linear Regression using nn.module model (Define a Class with _init_ ( includes nn.linear(1,1) and forward sections (returns nn.linear(1,1))

Example 5= Linear Regression using MLP (Multi Layer Perceptron)

 I wrote this code in Pycharm. Open new project, new python file and run the code line be line. Use breakpoints in training step and check if gradients are not zero after each step. In big deep Neural networks, you should check if gradients are not zero at first steps.

      Notes: 
      -Number of Hidden neurons are 10, dimention of input is 3 and there are two classes.
      -using sklearn.datasets import make_blobs to create data
      - 60% of Data are Training set, 15% is validation and 25% is Test data
      -use cross-entropy as loss function 
      -use nn.sequentional to define model and use  nn.Linear and then nn.Relu (to define activation function) to build layers.
      -compute Accuracy = num of correct classification/ total num of samples for Train, Validation and Test Data
      -pay attention why Accuracy for Test Data was computed after Loop of Training
      
      
      
     
      
Example 7= MLP for classification

       Notes: 
        -Use Dataset https://www.apispreadsheets.com/datasets/119


Example 6= 

   6-1) Generalization of Training step ( A function that get Loss, Model, Optimizer and return train step or corresponding Loss, this function will be used in training loop
   
   6_2) creating Dataset class ( it includes __init__(self), __len__(self), __get_item__(self, index), using _get_item, you load big dataset on demand) to use in Dataloader . Detaloader will create mini-batches of Data, will shuffle data. 

   6_3) Building Dataloader for test data and evaluation of model with test data

