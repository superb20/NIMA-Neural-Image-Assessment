# NIMA: Neural Image Assessment

This is a Keras implementation of the paper [NIMA: Neural Image Assessment(2017)](https://arxiv.org/pdf/1709.05424.pdf) by Hossein Talebi and Peyman Milanfar. You can find an introduction from [Google Research Blog](https://ai.googleblog.com/2017/12/introducing-nima-neural-image-assessment.html).

'NIMA' is a model that is trained to predict which images a typical user would rate as looking good (technically) or attractive (aesthetically).

Below is my mild stone.
1. Check the other open source.(Done)
2. Make estimate code.(Done)
3. Make train code. #TODO
4. Convert for Android version for performance test. #TODO
5. Make some application. #TODO
6. Refactoring and optimize. #TODO

# Implementation Details
+ The model was trained on the [AVA: A Large-Scale Database for Aesthetic Visual Analysis](http://refbase.cvc.uab.es/files/MMP2012a.pdf) by Naila Murray and Luca Marchesotti, which contains roughly 255,500 images. You can get it from [here](https://github.com/mtobeiyf/ava_downloader).
+ [TID2013](http://www.ponomarenko.info/tid2013.htm) used for technical ratings.

# Pretrained model
+ You can get models from [here](https://github.com/titu1994/neural-image-assessment/releases).

# Usage
## TRAIN
+ python train_mobilenet.py

## Evaluation
+ python evaluate_NIMA.py -img_dir test_images -img_resize true -network MobileNet -weight weights/mobilenet_weights.h5
+ python evaluate_NIMA.py -img_dir test_images -img_resize true -network NasNet -weight weights/nasnet_weights.h5
+ python evaluate_NIMA.py -img_dir test_images -img_resize true -network InceptionResNet -weight weights/inception_resnet_weights.h5

## convert h5 to tflite
+ python h5_to_tflite.py (TocoConverter is not working on Windows, I used [Colab](https://colab.research.google.com))



# Example Results


# References
1. Talebi, Hossein, and Peyman Milanfar. "NIMA: Neural Image Assessment." IEEE Transactions on Image Processing (2018).
2. "AVA: A Large-Scale Database for Aesthetic Visual Analysis." 
3. [Introducing NIMA: Neural Image Assessment](https://ai.googleblog.com/2017/12/introducing-nima-neural-image-assessment.html) - Googla AI Blog

