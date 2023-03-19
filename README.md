# YOLOv8-Instance-Segmentation

## Aim
This project utilizes YOLOv8 for the instance segmentation of fire. <br>

![1](https://user-images.githubusercontent.com/44557162/226201486-f5662449-15a4-4a0a-9be5-b2ce9b518271.gif)

## Dataset
Only one class named ```fire``` was used. A total of 250 images were used, consisting of 200 for training and 50 for validation. 
You can access the labeled data from [here](https://universe.roboflow.com/dlproject-2mzlq/yolo7_fire_3/browse?queryText=split%3Atrain&pageSize=50&startingIndex=0&browseQuery=true).

## Requirements
```
pip install ultralytics
```

## Evaluation
The graph below illustrates the values for mAP, loss, precision, and recall.
![results](https://user-images.githubusercontent.com/44557162/226199842-e040555a-df28-4f07-9444-bb688e6ddb13.png)


## Results
Run the following command:
```
!yolo task=segment mode=predict model=runs/segment/train3/weights/best.pt conf=0.25 source=dataset/test/y.mp4 save=true
```

Here is the final outcome: <br>

![y](https://user-images.githubusercontent.com/44557162/226201018-6062ee72-c42e-4622-8292-72334cf5c046.gif)
