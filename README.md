# ScriptIdentification
The aim of this repository is to identify script given an image in natural scene. Currently this repository provides inference code and the respective models. The models are fashioned as triplets with hindi and english as the common language in the triplet with the third language being the one of the below mentioned language. 

## Installation


## Inference

Script detection can be done using ```infer.py```.

```
python infer.py demo_images/D_image_149_9.jpg hinengodi
#{'predicted_class': 'odia'}
```

