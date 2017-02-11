# Chinese-Character-Recognition
This project shows how to use CNN to perform Chinese character recognition, a much more complicated task compared to MNIST digit recognition.

This code is based on a similar [repo](https://github.com/burness/tensorflow-101/tree/master/chinese_hand_write_rec/src), but is cleaner and outperforms that one: This code defines a data iterator class to deal with the data preprocessing and use 2 different input pipeline for training and testing data. 

Moreover, Training only 8000 steps achieves a top 1 accuracy of xxx and a top 3 accuracy of .

The repo owner kindly shared the [preprocessed dataset](https://pan.baidu.com/s/1o84jIrg#list/path=%2F)

For training, run:
---------------
`python --mode=train --max_steps=8002 --eval_steps=500 --save_steps=4000`
(Which is also the default parameter)

For validation, run:
--------------
`python --mode=validation`

