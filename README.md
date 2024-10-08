# gait_recognition
# Gait Recognition Silhouette Extraction
Overview:
This project focuses on using gait recognition to Identify people the extraction of human silhouettes from video files, which serves as the first step in developing a gait recognition system. The extracted silhouettes will be used as input for subsequent modeling processes.
After extracting the silhouettes, the next steps will involve training a gait recognition model using the segmented silhouettes as input data.

# Features of the human silhouette extracter:

Processes multiple videos from nested directories.
Utilizes a pretrained DeepLabV3 model for accurate silhouette segmentation.
Outputs processed videos containing only the extracted silhouettes.
Designed for efficient GPU utilization to accelerate processing.

# Setup and Installation:
Prerequisites:
Python 3.x
PyTorch
OpenCV
torchvision
numpy
Installation

Clone the repository:
```sh
git clone https://github.com/AlshangitiJumana/gait_recognition.git
cd gait_recognition
```
Install the required packages:

pip install torch torchvision opencv-python numpy
Usage
Directory Structure

Ensure your input data is structured as follows:

/path/to/Original_data/

    ├── 001/
    │   ├── video1.mp4
    │   ├── video2.mp4
    ├── 002/
    │   ├── video3.mp4
    │   ├── video4.mp4
    └── ...
The data in the `Original_data` directory consists of videos recorded with my phone, featuring four different people walking towards and away from the camera.
It is recommended to take six videos for each person.
# Running the Code

Update the input_dir and output_dir variables in the script to match your directory paths. 

I recommend using a Kaggle notebook to run the code, as it provides free GPU access for up to 30 hours a week, which will significantly speed up the processing compared to running it on a CPU.

Execute the script to extract silhouettes from the videos.

Output
Processed videos will be saved in the specified output directory, with filenames prefixed by output-{file-name}.

# gait_recognition

## Gait Recognition Silhouette Extraction

### Overview
This project focuses on using gait recognition to Identify people the extraction of human silhouettes from video files, which serves as the first step in developing a gait recognition system. The extracted silhouettes will be used as input for subsequent modeling processes.

After extracting the silhouettes, the next steps will involve training a gait recognition model using the segmented silhouettes as input data.

### Features of the Human Silhouette Extractor
- Processes multiple videos from nested directories.
- Utilizes a pretrained DeepLabV3 model for accurate silhouette segmentation.
- Outputs processed videos containing only the extracted silhouettes.
- Designed for efficient GPU utilization to accelerate processing.

### Setup and Installation
#### Prerequisites
- Python 3.x
- PyTorch
- OpenCV
- torchvision
- numpy

#### Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/AlshangitiJumana/gait_recognition.git
    cd gait_recognition
    ```

2. Install the required packages:
    ```sh
    pip install torch torchvision opencv-python numpy
    ```

### Usage
#### Directory Structure
Ensure your input data is structured as follows:

/path/to/Original_data/

    ├── 001/
    │   ├── video1.mp4
    │   ├── video2.mp4
    ├── 002/
    │   ├── video3.mp4
    │   ├── video4.mp4
    └── ...


#### Running the Code
1. Update the `input_dir` and `output_dir` variables in the script to match your directory paths.

2. Execute the script to extract silhouettes from the videos.

#### Output
Processed videos will be saved in the specified output directory, with filenames prefixed by `output-{file-name}`.

### Next Steps
After silhouette extraction, the next step is to turn the video into frames of size 64x64,
similar to what was done with Dataset-B in the GaitSet repository.

#### Using GaitSet Preparation Code for CASIA-B Dataset

1. Follow the instructions in the GaitSet repository to prepare the dataset:
    ```sh
    git clone https://github.com/AbnerHqC/GaitSet.git
    cd GaitSet
    ```

2. Use the provided preparation script to convert the video into frames:
    ```sh
    python prepare_dataset.py --input_dir /path/to/output-silhouettes --output_dir /path/to/frames --frame_size 64
    ```

#### for you videos run the Code silhouette-cut-code.ipynb
1. Load the Jupyter notebook provided in the repository:
    ```sh
    jupyter notebook silhouette-cut-code.ipynb
    ```

2. Follow the instructions in the notebook to process the frames and prepare them for model training.

### Notes
I recommend using a Kaggle notebook to run the code, as it provides free GPU access for up to 30 hours a week, which will significantly speed up the processing compared to running it on a CPU.

## Acknowledgment 
I used the Gaitset code and paper as a reference in this project
@ARTICLE{chao2019gaitset,
  author={Chao, Hanqing and Wang, Kun and He, Yiwei and Zhang, Junping and Feng, Jianfeng},
  journal={IEEE Transactions on Pattern Analysis and Machine Intelligence}, 
  title={GaitSet: Cross-view Gait Recognition through Utilizing Gait as a Deep Set}, 
  year={2021},
  pages={1-1},
  doi={10.1109/TPAMI.2021.3057879}}

  and for the Silhouette extraction code I used this code as reference 
  
  https://github.com/jordankzf/human-silhouette-extractor.git
