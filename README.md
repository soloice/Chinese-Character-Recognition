# Chinese-Character-Recognition
This tensorflow project shows how to use CNN to perform Chinese character recognition, a much more complicated task compared to digit recognition.

This code is based on a similar [repo](https://github.com/burness/tensorflow-101/tree/master/chinese_hand_write_rec/src), but is cleaner and outperforms that one: This code defines a data iterator class to deal with the data preprocessing and use 2 different input pipeline for training and testing data. 

Moreover, Training only 12000 steps (~8 hour on my workstation with 8 CPU cores and 32 GB RAM) achieves a top 1 accuracy of 82.8% and a top 3 accuracy of 92.7%. If you have a GPU card, it should be much more faster.

The repo owner above also kindly shared the [preprocessed dataset](https://pan.baidu.com/s/1o84jIrg#list/path=%2F)

For training, run:
---------------
`python --mode=train --max_steps=12002 --eval_steps=50 --save_steps=4000`

For validation, run:
--------------
`python --mode=validation`

