 RBM_example
 ===========
 
 Example of RBM using python and tensorflow

# Overview

    * Use code from existing books
    * RBM implementation using Python and tensor flow
    * Confirm the difference between each method
    * Simple usage example

# Origin

* python code : Machine Learning: An Algorithmic Perspective, Second Edition by Stephen Marsland

![algo](https://user-images.githubusercontent.com/37811577/55819714-51c80200-5b34-11e9-8e02-86b5ba9644d5.jpg)

* tensorflow code : TensorFlow 1.x Deep Learning Cookbook by Antonio Gulli, Amita Kapoor

![purple](https://user-images.githubusercontent.com/37811577/55819740-5f7d8780-5b34-11e9-97d1-206b6d9f6dac.jpg)

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

![algo_figure_ex1](https://user-images.githubusercontent.com/37811577/55819725-55f41f80-5b34-11e9-9604-37c2bb6bfe33.png)

  
 
 * tensorflow
 
![mnist_figure_ex1](https://user-images.githubusercontent.com/37811577/55819732-5b516a00-5b34-11e9-8a42-84178ecd2b7b.png)
 
 
# parameters/hyper parameters

* python : 

      nVisible = 5, nHidden = 2, nlabels = None, eta = 0.1, decay = 0, nCDsteps = 5, momentum - 0.9, nepochs = 1000

* tensorflow : 

      Visible = Xtrain.shape[1], Hidden = 100, epochs = 1, batch_size = 100

