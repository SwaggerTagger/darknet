# Our Modifications to Darknet
## Machine Readable Output
Have darknet output machine readable (json) predictions instead of writing the results directly to the bounding boxes of an image.
For this purpose `darknet detector` now recognizes the `-tagger-output` switch, which will disable all writes to stdout except when the predictions are written.
Example:
```bash
./darknet detector test cfg/coco.data cfg/yolo.cfg yolo.weights data/dog.jpg -tagger-output 2>/dev/null
{"input": "data/dog.jpg", "time": 13.036422, "matches": [
{"class": "dog", "probability": 0.823520, "left": 132, "right": 321, "top": 231, "bottom": 521 }
, {"class": "truck", "probability": 0.643006, "left": 467, "right": 680, "top": 84, "bottom": 168 }
, {"class": "bicycle", "probability": 0.852180, "left": 95, "right": 588, "top": 123, "bottom": 448 }
], "count": 3 }
```

![Darknet Logo](http://pjreddie.com/media/files/darknet-black-small.png)

#Darknet#
Darknet is an open source neural network framework written in C and CUDA. It is fast, easy to install, and supports CPU and GPU computation.

For more information see the [Darknet project website](http://pjreddie.com/darknet).

For questions or issues please use the [Google Group](https://groups.google.com/forum/#!forum/darknet).
