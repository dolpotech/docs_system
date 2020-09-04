#Structuring the documentation

##Principle  
Documentations will be mainly based on modular system. A module can represent the entire system or mean a smaller system inside a system. For example Measurement module, Notification module

## Documentation body

The modular system itself can be very vague. So we will be breaking it down in a systematic fashion for clear understanding. The following aspect should be covered while explaining a module.

### General overview
This section includes the introduction of the module with  various other aspect such as :

- The previous module it was related to
- A short brief of what is going to happen inside the module
- The next module it is going to relate to

### Architecture and data flow 

Here the general idea of the module is discussed more technically.
Explanation of absolute data flow can be confusing and can create misunderstanding. So to provide the clear picture of the module, it is recommended to make the explanation relative. By relative, it means to explain the following aspect

- Input and its format : where the data has come from and what format it supports
- Processing : what is going to happen inside the module and how the data is going to be processed.
- Output and its format : what data it provides and what are the format



Let's see how we will be doing it.
The architecture and data flow section is broken down into following sections.

##### Architecture / data flow diagrams
##### Data flow processes
##### Module components


### Classes and methods

Provide information about the classes the module holds and their methods.

### Database schema

The detail discussion about database schema and tables.

Any field that accepts data of specific format should be defined properly.
For example, The joint field accepts a json format containing the following data structure.

```
[
    {
      "confidence" : 0.90087890625,
      "name" : "leftWrist",
      "position" : [
        887.125,
        767.1398635477583
      ]
    },
    {
      "position" : [
        711.39035087719299,
        167.38596491228068
      ],
      "name" : "leftEar",
      "confidence" : 0.9814453125
    },
    {
      "confidence" : 0.7568359375,
      "position" : [
        690.90515350877195,
        1353.3343079922026
      ],
      "name" : "leftAnkle"
    },
    {
      "position" : [
        647.06597222222217,
        160.48026315789474
      ],
      "name" : "nose",
      "confidence" : 1
    },
    {
      "confidence" : 1,
      "name" : "leftEye",
      "position" : [
        679.38706140350871,
        137.38109161793372
      ]
    },
    {
      "name" : "rightShoulder",
      "position" : [
        491.95663148757308,
        339.77655945419099
      ],
      "confidence" : 0.99462890625
    },
    {
      "name" : "rightAnkle",
      "confidence" : 0.7880859375,
      "position" : [
        446.38404605263156,
        1345.7300194931772
      ]
    },
    {
      "confidence" : 1,
      "name" : "rightEye",
      "position" : [
        624.60526315789468,
        135.80068226120858
      ]
    },
    {
      "position" : [
        766.35252192982455,
        354.55997197855748
      ],
      "confidence" : 0.9951171875,
      "name" : "leftShoulder"
    },
    {
      "name" : "rightKnee",
      "confidence" : 0.951171875,
      "position" : [
        481.69846491228066,
        1062.1839668615985
      ]
    },
    {
      "confidence" : 0.98486328125,
      "name" : "rightElbow",
      "position" : [
        413.80528143274853,
        546.23757309941516
      ]
    },
    {
      "name" : "rightHip",
      "confidence" : 0.87158203125,
      "position" : [
        524.74744152046776,
        741.55555555555554
      ]
    },
    {
      "confidence" : 0.98681640625,
      "position" : [
        817.62134502923971,
        576.51730019493175
      ],
      "name" : "leftElbow"
    },
    {
      "position" : [
        699.72624269005848,
        1105.9658869395712
      ],
      "confidence" : 0.88916015625,
      "name" : "leftKnee"
    },
    {
      "position" : [
        584.23825840643269,
        164.47709551656919
      ],
      "confidence" : 0.9921875,
      "name" : "rightEar"
    },
    {
      "confidence" : 0.873046875,
      "name" : "leftHip",
      "position" : [
        700.2072368421052,
        751.86257309941516
      ]
    },
    {
      "confidence" : 0.962890625,
      "name" : "rightWrist",
      "position" : [
        334.66885964912279,
        730.97368421052624
      ]
    }
  ]
```

### External data dependencies `(If any)`
The external files that the system expectes should be clearly defined. This is going to help those who are working on different technology on the same system. 

#### ZIP example

In case of image capture, a zip file including the depth data images and its corresponding data are sent.
So the details that are to be included are : 

##### Directory structure

```
└───{unique_id}.zip
        └───{unique_id}    
                ├───data.json                   | include sample of data.json
                ├───{pose_id}-{file_name}.png   | where "-" is the seperator
                └───{pose_id}-{file_name}.json  | include sample of .json file
```

!!! info
    Same file_name ensures the relation between image and file.


### References

Any tutorials or external references that are to be taken under consideration.

## Sample documentations

1. [Notification system](../../sample_documentations/notification/pages/notification.md)

