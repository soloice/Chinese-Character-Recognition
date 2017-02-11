# Chinese-Character-Recognition
This tensorflow project shows how to use CNN to perform Chinese character recognition, a much more complicated task compared to digit recognition.

This code is based on a similar [repo](https://github.com/burness/tensorflow-101/tree/master/chinese_hand_write_rec/src), but is cleaner and outperforms that one: This code defines a data iterator class to deal with the data preprocessing and use 2 different input pipeline for training and testing data. 

Moreover, Training only 8000 steps (~5 hour on my workstation with 8 CPU cores and 32 GB RAM) achieves a top 1 accuracy of 69.3% and a top 3 accuracy of 83.9%. If you have a GPU card, it should be much more faster.

The repo owner kindly shared the [preprocessed dataset](https://pan.baidu.com/s/1o84jIrg#list/path=%2F)

For training, run:
---------------
`python --mode=train --max_steps=8002 --eval_steps=500 --save_steps=4000`

For validation, run:
--------------
`python --mode=validation`

