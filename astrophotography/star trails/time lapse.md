---
title: Time Lapse
layout: default
parent: Star Trails
grand_parent: Astrophotography
nav_order: 1
---

## Time Lapse

<br>

### Code

The following code is written in python. Install the dependencies using:

```sh
pip3 install opencv-python
```

Save the following code in a file named `time_lapse.py`:

```py
# Imports
import cv2
import os

input_folder = "" # Enter the absolute path of the input folder
output_file = "" # Enter the absolute path of the output file
frame_interval = 1 # Every n-th frame will be considered

# Get a list of image files in the input folder
image_files = [
    f for f in os.listdir(input_folder) if f.endswith((".jpg", ".jpeg", ".png"))
]
image_files.sort()  # Sort the files to ensure correct order

# Get the first image to get dimensions for video creation
first_image = cv2.imread(os.path.join(input_folder, image_files[0]))
height, width, layers = first_image.shape

# Define the codec and create VideoWriter object
fourcc = cv2.VideoWriter_fourcc(*"mp4v")  # You can change the codec as needed
video = cv2.VideoWriter(output_file, fourcc, 30, (width, height))

# Iterate through image files and create video
for i, image_file in enumerate(image_files):
    if i % frame_interval == 0:  # Consider every nth frame
        image_path = os.path.join(input_folder, image_file)
        frame = cv2.imread(image_path)
        video.write(frame)

# Release the VideoWriter object and close any open windows
video.release()
cv2.destroyAllWindows()
```

Enter the value of the variables, namely, `input_folder`, `output_file` and `frame_interval` and run the code using:

```sh
python3 time_lapse.py
```
