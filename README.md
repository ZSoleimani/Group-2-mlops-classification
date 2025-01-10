# Group-2-mlops-classification
Group 2: Project for 02476 Machine Learning Operations (DTU Course)

## Project goal
This project aims to classify images of various PC parts using a deep learning model, specifically leveraging the power of Albumentations for data augmentation to improve model robustness. The dataset used for this project is the PC Parts Images Dataset from Kaggle, which contains images of different computer components (e.g., motherboards, RAM, graphics cards, etc.).

## Third-party package 
The third-party package used in this project is [albumentations](https://github.com/albumentations-team/albumentations), which is an image augmentation library written in Python. Albumentation has +70 augmentations that can be applied to the training data, involving transformations such as JPEG compression, blurring, grayscaling, channel shuffling, RGB switching, and more. The documentation can be found [here](https://albumentations.ai/docs/). 

## Data description
The dataset initially used for this project is the [PC Parts Images Dataset](https://www.kaggle.com/datasets/asaniczka/pc-parts-images-dataset-classification?select=pc_parts) from Kaggle, consisting of 3,279 images categorized into 14 distinct classes: 
- cables
- case
- cpu
- gpu
- hdd
- headset
- keyboard
- microphone
- monitor
- motherboard
- mouse
- ram
- speakers
- webcam

The total size of the dataset is approximately 36 MB, where each image has a resolution of 256x256 pixels and formatted in the JPG file type. This consistency allows for simple application of data augmentation techniques to the images, creating a larger and more diverse datasets. 
Each class contains between 142 and 298 images, providing a relatively balanced representation of PC parts which is needed for training a robust model and reduces the models likelihood of bias towards a specific class. This dataset is therefore, very suitable for a multi class classification task. 

## Models
Our primary focus will be on developing a simple convolutional neural network (CNN) architectur for the image classification task. The CNN will include layers for feature extraction (convolutional and pooling layers) and fully connected layers for classification. To optimize performance, we will experiment with the network architecture and hyperparameter settings using the tools provided in 02476. If needed, we might explore transfer learning using pre-trained models such as MobileNet or ResNet and fine-tuning them; we might also instead just experiment with the third party package, Albumentation, where two identical models are trained (one uses Albumentaion and one doesn't)and compared to quantify the efficacy of albumentation.


## Project structure

The directory structure of the project looks like this:
```txt
├── .github/                  # Github actions and dependabot
│   ├── dependabot.yaml
│   └── workflows/
│       └── tests.yaml
├── configs/                  # Configuration files
├── data/                     # Data directory
│   ├── processed
│   └── raw
├── dockerfiles/              # Dockerfiles
│   ├── api.Dockerfile
│   └── train.Dockerfile
├── docs/                     # Documentation
│   ├── mkdocs.yml
│   └── source/
│       └── index.md
├── models/                   # Trained models
├── notebooks/                # Jupyter notebooks
├── reports/                  # Reports
│   └── figures/
├── src/                      # Source code
│   ├── project_name/
│   │   ├── __init__.py
│   │   ├── api.py
│   │   ├── data.py
│   │   ├── evaluate.py
│   │   ├── models.py
│   │   ├── train.py
│   │   └── visualize.py
└── tests/                    # Tests
│   ├── __init__.py
│   ├── test_api.py
│   ├── test_data.py
│   └── test_model.py
├── .gitignore
├── .pre-commit-config.yaml
├── LICENSE
├── pyproject.toml            # Python project file
├── README.md                 # Project README
├── requirements.txt          # Project requirements
├── requirements_dev.txt      # Development requirements
└── tasks.py                  # Project tasks
```
