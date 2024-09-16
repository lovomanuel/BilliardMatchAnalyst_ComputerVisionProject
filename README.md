# BilliardFinalProject

## Project Description
This project focuses on various computer vision tasks related to billiards, including ball segmentation and classification, tracking, and metrics computation. The project is divided into several executable components, each handling specific aspects of the task.

## Requirements
- CMake (version 3.5 or higher)
- OpenCV (ensure it is installed and available in your system)

## Project Structure
Final_Project_CV_codes/
├── include/ # Header files
├── src/ # Source files
│ ├── Main_Field_Balls.cpp //Done by me
│ ├── Balls_segmentation.cpp //Done by me
│ ├── ball_classification.cpp
│ ├── Classes.cpp //Done by me
│ ├── Field_detection.cpp //Done by me
│ ├── Utilities.cpp //Done by me
│ ├── Metrics.cpp //Done by me
│ ├── main_tracking.cpp
│ ├── tracking.cpp
│ ├── table_orientation.cpp
│ ├── Main_metrics.cpp //Done by me
│ ├── main.cpp
├── CMakeLists.txt
└── README.md

## Building the Project
Clone the repository and enter inside the folder with cd command

mkdir build
cd build

cmake ..

make

# Video Processing Project

## Folder Organization

The project is organized into the following folders:

- `src`: Contains the C++ source files.
- `include`: Contains the header files.
- `Input_videos`: Contains the input videos.
- `Output_videos`: Where processed videos are saved.
- `First_frames_images`: Contains the first frame of each video.
- `First_frames_detected_bboxes`: Contains the bounding boxes computed for the first frame of the videos, saved in a txt file following the same format as the ground truth.
- `First_frames_truth_bboxes`: Contains txt files for the ground truth of the bounding boxes for the first frame.
- `First_frames_truthmasks`: Contains the ground truth masks for the first frames.
- `Last_frames_detected_bboxes`: Contains the bounding boxes computed for the last frame of the videos, saved in a txt file following the same format as the ground truth.
- `Last_frame_2D_maps`: Contains the last frame of the video with 2D representation saved here.
- `Last_frames_images`: Contains the last frame of each video.
- `Last_frames_truthmasks`: Contains the ground truth masks for the last frames.
- `Table_vertices`: Contains txt files with the vertices of the table computed in the segmentation task.

## Required Folders for Execution

The program requires the following folders to be populated for the segmentation, classification, and tracking system tasks to work:

- `Input_videos`
- `First_frames_images`
- `Last_frames_images`

For metrics computation, the ground truth folders also need to be populated.

## Building the Project

The `CMakeLists.txt` file is provided in the main folder of the project. The project defines four executables:

- `complete`: Executes all project tasks.
- `segmentation_and_classification`: Executes segmentation and classification tasks.
- `tracking`: Executes the tracking system (only after `segmentation_and_classification` execution).
- `metrics`: Executes metrics computation (only after `tracking` execution).

To build the project, follow these steps:

1. Navigate to the main folder of the project:
   ```sh
   cd path/to/project

# IMPORTANT DISCLAIMER

This project has been developed by three different people. Each member of the group had different tasks. However, for the correctness of the code, I have updated all the codes, including those that were not developed by me.

I have specifically developed the codes for detecting the field of the billiard table, detecting and segmenting all balls inside different videos, and computing the metrics.

 If you prefer not to run the code, I have also uploaded a report detailing the ideas (only for my parts) used and other relevant information and a folder containing output videos obtained by tracking system (not developed by me).

