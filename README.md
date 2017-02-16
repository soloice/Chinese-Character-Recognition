# Chinese-Character-Recognition
This tensorflow project shows how to use CNN to perform Chinese character recognition, a much more complicated task compared to digit recognition.

This code is based on a similar [repo](https://github.com/burness/tensorflow-101/tree/master/chinese_hand_write_rec/src), but is cleaner and outperforms that one: This code defines a data iterator class to deal with the data preprocessing and use 2 different input pipeline for training and testing data. 

Moreover, Training only 12000 steps (~8 hour on my workstation with 8 CPU cores and 32 GB RAM) achieves a top 1 accuracy of 82.8% and a top 3 accuracy of 92.7%. If you have a GPU card, it should be much more faster.

The repo owner above also kindly shared the [preprocessed dataset](https://pan.baidu.com/s/1o84jIrg#list/path=%2F)

For training, run:
---------------
`python chinese_character_recognition.py --mode=train --max_steps=12002 --eval_steps=50 --save_steps=4000`

For validation, run:
--------------
`python chinese_character_recognition.py --mode=validation`


For the version using batch normalization, run:
---------------

`python chinese_character_recognition_bn.py --mode=train --max_steps=8002 --eval_steps=100 --save_steps=1000`

or

`python chinese_character_recognition_bn.py --mode=validation`

After training only 8000 mini-batches, which takes ~16h on my workstation, gives a top 1 accuracy of 90.26% and top 3 accuracy of 96.48%. Note that the network hasn't fully convergenced yet (though almost), so training for a longer time should be able to improve the performance furthur. As reported in [this project report](http://cs231n.stanford.edu/reports/zyh_project.pdf), the network has the potential to achieve a top 1 accuracy of 95% when properly trained (maybe even better, since in the aforementioned paper they didn't use batch normalization, which should improve generalization capacity of the network). So if you have a powerful GPU, run more training steps.

This is [my checkpoint](https://pan.baidu.com/s/1o7CJrBW) at step 8000. If you want to try it on your laptop or something else, feel free to do so!


I also attached the learning curve of `chinese_character_recognition_bn.py`:

![accuracy-bn](https://github.com/soloice/Chinese-Character-Recognition/blob/master/accuracy-bn.PNG)

![loss-bn](https://github.com/soloice/Chinese-Character-Recognition/blob/master/loss-bn.PNG)

