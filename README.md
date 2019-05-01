
# Introduction
  Thanks for these projects, this work now is support tiny_yolo v3 but only for test, if you want to train you can either train a model in darknet or in the second following works. It also can tracks many objects in coco classes, so please note to modify the classes in yolo.py. besides, you also can use camera for testing.

  https://github.com/nwojke/deep_sort

  https://github.com/qqwweee/keras-yolo3

  https://github.com/Qidian213/deep_sort_yolov3

# Quick Start

1. Download YOLOv3 or tiny_yolov3 weights from [YOLO website](http://pjreddie.com/darknet/yolo/).Then convert the Darknet YOLO model to a Keras model. Or use what i had converted https://drive.google.com/file/d/1uvXFacPnrSMw6ldWTyLLjGLETlEsUvcE/view?usp=sharing (yolo.h5 model file with tf-1.4.0) , put it into model_data folder
2. Run YOLO_DEEP_SORT with cmd :
   ```
   python demo.py
   ```

3. (Optional) Convert the Darknet YOLO model to a Keras model by yourself:

  ```
   please download the weights at first from yolo website.
   python convert.py yolov3.cfg yolov3.weights model_data/yolo.h5
  ```

# Dependencies

  The code is compatible with Python 2.7 and 3. The following dependencies are needed to run the tracker:

    NumPy
    sklean
    OpenCV
    Pillow
  This code works on TensorFlow-1.8.0

# Training the model

  To train the deep association metric model on your datasets you can reference to https://github.com/nwojke/cosine_metric_learning  approach which is provided as a separate repository.

  Be careful that the code ignores everything but person. For your task do not forget to change :

  [deep_sort_yolov3/yolo.py]   Lines 100 to 101 :

          if predicted_class != 'person' :
               continue



# Result

 Links to the results are provided in the result.txt
