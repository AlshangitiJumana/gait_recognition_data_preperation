# gait_recognition
Gait Recognition Silhouette Extraction
Overview:
This project focuses on using gait recognition to Identify people the extraction of human silhouettes from video files, which serves as the first step in developing a gait recognition system. The extracted silhouettes will be used as input for subsequent modeling processes.
After extracting the silhouettes, the next steps will involve training a gait recognition model using the segmented silhouettes as input data.

Features of the human silhouette extracter:
Processes multiple videos from nested directories.
Utilizes a pretrained DeepLabV3 model for accurate silhouette segmentation.
Outputs processed videos containing only the extracted silhouettes.
Designed for efficient GPU utilization to accelerate processing.
Setup and Installation:
Prerequisites:
Python 3.x
PyTorch
OpenCV
torchvision
numpy
Installation
Clone the repository:
git clone https://github.com/AlshangitiJumana/gait_recognition.git
cd gait_recognition
Install the required packages:

Copy code
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
Running the Code
Update the input_dir and output_dir variables in the script to match your directory paths. 
I recommend using a Kaggle notebook to run the code, as it provides free GPU access for up to 30 hours a week, which will significantly speed up the processing compared to running it on a CPU.

Execute the script to extract silhouettes from the videos.

Output
Processed videos will be saved in the specified output directory, with filenames prefixed by output-{file-name}.


