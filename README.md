# Datasets-and-Iterators
This repository contains code examples for TensorFlow's new data pipelines. This is the support repository for the blog https://medium.com/@animeshblog/building-efficient-data-input-pipelines-using-tensorflow-8f647f03b4ce

Most of the introductory articles on TensorFlow would introduce you with the **feed_dict** method of feeding the data to the model. 
**feed_dict** processes the input data in a single thread and while the data is being loaded and processed on CPU, the GPU remains 
idle and when the GPU is training the first batch of data, CPU remains in idle state. The developers of TensorFlow have advised not 
to use this method during training or repeated validation of same datasets.

![alt text](https://github.com/animesh-agarwal/Datasets-and-Iterators/blob/master/images/feed_dict.PNG)

**tf_data** improves the performance by prefetching the next batch of data asynchronously so that GPU need not wait for the data. 
You can also parallelize the process of preprocessing and loading the dataset.

![alt text](https://github.com/animesh-agarwal/Datasets-and-Iterators/blob/master/images/tf_data.PNG)

**What is covered?** 

* How to create datasets 
* How to apply different transformations on the dataset
* Creating Iterators
* Using different iterators with MNIST Example
