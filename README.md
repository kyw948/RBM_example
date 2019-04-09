 RBM_example
 ===========
 
 Example of RBM using python and tensorflow

# Overview

    * Use code from existing books
    * RBM implementation using Python and tensor flow
    * Confirm the difference between each method
    * Simple usage example

# origin

* tensorflow code : TensorFlow 1.x Deep Learning Cookbook by Antonio Gulli, Amita Kapoor


* python code : Machine Learning: An Algorithmic Perspective, Second Edition by Stephen Marsland

# reference

* RBM implementation : https://www.cs.toronto.edu/~hinton/absps/guideTR.pdf


# Example

* python : 

<code>
  
    import algo_rbm
    
    algo_rbm.learn_letters()
  
    ....
  
    import algo_rbm as rbm
  
    rb = rbm.rbm(20*16,50,nlabels=None,eta=0.3,momentum=0.5,nCDsteps=3,nepochs=1000)
  
</code>



* tensorflow : 

<code>
    
    import RBM
    
    mnist = input_data.read_data_sets("MNIST_data/", one_hot=True)
    trX, trY, teX, teY = mnist.train.images, mnist.train.labels, mnist.test.images, mnist.test.labels
    
    ...
    
   _, m = Xtrain.shape
  
    rbm = RBM.RBM(m, 100)
   
</code>


# output :


* python 

![Alt text](/path/to/algo_figure_ex1.png)
 
 
 
 * tensorflow
 
 ![Alt text](/path/to/mnist_figure_ex1.png)
 
 
# parameters/hyper parameters

* python : 

      nVisible = 5, nHidden = 2, nlabels = None, eta = 0.1, decay = 0, nCDsteps = 5, momentum - 0.9, nepochs = 1000

* tensorflow : 

      Visible = Xtrain.shape[1], Hidden = 100, epochs = 1, batch_size = 100

