This script processes images to detect body keypoints using MediaPipe's Pose model and stores the results in a CSV file.

Requirements
Python 3.x
OpenCV
MediaPipe
You can install the required packages using:

bash
Copy code
pip install opencv-python mediapipe
Usage
Place your images in a folder. Supported formats: JPG, JPEG, PNG, GIF.

Update the paths in the script:

folder_path: Path to the folder containing the images.
output_filename: Path to the output CSV file where keypoints will be saved.
Run the script:

bash
Copy code
python your_script_name.py
Script Details
Function detect_body_keypoints(image_path):

Loads an image from the given path.
Converts the image to RGB.
Processes the image to detect body keypoints using MediaPipe.
Returns keypoints as a list of coordinates.
Function store_image_keypoints(folder_path, output_filename):

Iterates through all images in the specified folder.
Detects body keypoints for each image.
Writes keypoints to a CSV file with columns for each keypoint's x, y, and z coordinates.
CSV File Format
The resulting CSV file will have the following columns:

file_name: Name of the image file.
Keypoint_i_x, Keypoint_i_y, Keypoint_i_z: X, Y, and Z coordinates for each keypoint (i from 1 to 33).
Example
To process images located in /content/drive/MyDrive/Dataset(colpro)/falling and save the results to /content/second.csv, set folder_path and output_filename accordingly in the script.
