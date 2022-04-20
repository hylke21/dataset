
# How to use the xml_to_csv.py


# How to use the generate_tfrecord.py

Now that we have generated our annotations and split our dataset into the desired training and testing subsets, 
it is time to convert our annotations into the so called TFRecord format.

Convert *.xml to *.record

Basically, you can just download the python file of generate_tfrecord.py. And here we will change it at command prompt.
Put the python file at your folder of train and test folder. Then, 'cd' your command prompt at the image folder. 

Create train data:
```python
python generate_tfrecord.py -x [PATH_TO_IMAGES_FOLDER]/train -l [PATH_TO_ANNOTATIONS_FOLDER]/label_map.pbtxt 
   -o [PATH_TO_ANNOTATIONS_FOLDER]/train.record
```

Create test data:
```python
python generate_tfrecord.py -x [PATH_TO_IMAGES_FOLDER]/test -l [PATH_TO_ANNOTATIONS_FOLDER]/label_map.pbtxt 
   -o [PATH_TO_ANNOTATIONS_FOLDER]/test.record
```

For example

```python

python generate_tfrecord.py -x C:/Users/sglvladi/Documents/Tensorflow/workspace/training_demo/images/train -l 
   --C:/Users/sglvladi/Documents/Tensorflow/workspace/training_demo/annotations/label_map.pbtxt -o 
   --C:/Users/sglvladi/Documents/Tensorflow/workspace/training_demo/annotations/train.record
 python generate_tfrecord.py -x C:/Users/sglvladi/Documents/Tensorflow/workspace/training_demo/images/test -l 
   --C:/Users/sglvladi/Documents/Tensorflow2/workspace/training_demo/annotations/label_map.pbtxt -o 
   --C:/Users/sglvladi/Documents/Tensorflow/workspace/training_demo/annotations/test.record
   
```
