# Samples

## Dataset
We have provided a sample directory structure for dataset used for training the models.

##### How is a dataset directory structured?

```text
dataset
├── 001
│   ├── a.jpg
│   └── b.jpg
└── 002
    └── a.jpeg
```

The above directory structure is taken from `FaceGateCore/samples/dataset` directory. Here are some important points to remember in directory tree:

1. `FaceGateCore/data/` is the root dirpath. 
2. `[DIR] dataset/` is the training dataset directory that must be present in `FaceGateCore/data/` dirpath. This will contain complete dataset that will be used for training custom models.
3. `[DIR] 001` 
    3.1 `[DIR] 001` represents the unique name for the person, whose images are to be used for training. Example: All images for Dr. APJ Abdul kalam are placed in `001` sample dataset directory.
    3.2 `[DIR] 001` can be any random name as long as it contains 1 or more images for a unique person. **Warn**: Do not place face pics of 2 different people in one directory each directory will represent only 1 individual with N images where N >= 1.
4. `[FILE] a.jpg` is the picture of the individual.
    4.1 `[FILE] a.jpg` If any picture doesn't contain the face of a human, it will be skipped automatically. 
    4.2 `[FILE] a.jpg` Faces will be automatically cropped from complete picture during training