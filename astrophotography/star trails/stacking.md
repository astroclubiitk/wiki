---
title: Stacking
layout: default
parent: Star Trails
grand_parent: Astrophotography
nav_order: 2
---

## Stacking

<br>

### Code

The following code is written in python. Install the dependencies using:

```sh
pip3 install numpy opencv-python
```

Save the following code in a file named `stacking.py`:

```py
# Imports
import cv2
import numpy as np
import os

input_folder = "" # Enter the absolute path of the input folder
output_file = "" # Enter the absolute path of the output file
frame_interval = 1 # Every n-th frame will be considered

# Get a list of image files in the input folder
image_files = [
    f for f in os.listdir(input_folder) if f.endswith((".jpg", ".jpeg", ".png"))
]
image_files.sort()  # Sort the files to ensure correct order

# Load the first image to get dimensions
first_image = cv2.imread(os.path.join(input_folder, image_files[0]))
height, width, _ = first_image.shape

# Initialize an empty image to accumulate star trails
star_trail = np.zeros((height, width, 3), np.uint8)

# Iterate through image files and accumulate star trails
for i, image_file in enumerate(image_files):
    if i % frame_interval == 0:  # Consider every nth frame
        image_path = os.path.join(input_folder, image_file)
        frame = cv2.imread(image_path)
        star_trail = cv2.max(star_trail, frame)  # "lighten" blending mode

# Save the resulting star trail image
cv2.imwrite(output_file, star_trail)
```

Enter the value of the variables, namely, `input_folder`, `output_file` and `frame_interval` and run the code using:

```sh
python3 stacking.py
```
