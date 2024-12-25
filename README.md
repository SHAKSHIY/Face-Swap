# Face Swap: 

A face-swapping tool to swap the face in a video with the face in a photo. A folder of photos, where each photo swaps over the folder of videos, outputs the face-swapped videos. If you are a developer, you are encouraged to go through the code.

# Google Colab:

This project can also be run on Google Colab. Ensure proper setup of file directories as mentioned below.

# Packages Installation:

To use this project, ensure the following packages are installed:

- cv2 (OpenCV)
- numpy (gets installed with OpenCV by default)
- dlib
- moviepy
- Built-in modules: os, glob

Install the required packages using pip:
pip install opencv-python numpy dlib moviepy

# How to Use:

Clone the repository to your local machine:
git clone <repository_url>
Ensure the following files and folders are in the project directory:
photos/: Folder containing the photos (use .jpg format).
videos/: Folder containing the videos (use .mp4 format).
shape_predictor_68_face_landmarks.dat: Pre-trained facial landmark model.
Add photos to the photos/ folder and videos to the videos/ folder.
Open the project folder in your Python IDE and run the script:
python main.py

Grab a glass of water while the code processes your inputs. 😄

# Result:

After execution, a result folder will be created in the project directory, containing all face-swapped videos. For example:
If there are 4 photos and 3 videos, the result folder will contain 12 face-swapped videos (4 photos × 3 videos).
Example Output
Input Video:
video.mp4

Input Photo:
photo1.jpeg

Face Swapped Result:
video_PHOTO.mp4

# Code Overview
The script processes the following steps:

Load Files: Reads photos and videos from the respective folders.

Face Detection: Uses dlib to detect faces and extract 68 facial landmarks.

Delaunay Triangulation: Maps triangles of the source face onto the target face.

Warping: Warps the triangles of the source face to match the target face.

Seamless Cloning: Integrates the swapped face onto the original video frame using OpenCV’s seamless cloning.

Audio Integration: Merges the original video’s audio with the processed video.

Output: Saves the resulting face-swapped videos in the result folder.

For further details, refer to the code in main.py.
