# Traffic Light Classifier

## Overview
In this project, I use knowledge of computer vision techniques to build a classifier for images of traffic lights to identify which is red, yellow, or green.
<img width="623" alt="all-lights" src="https://user-images.githubusercontent.com/48291391/61484597-322f4980-a96d-11e9-83bc-bf1cf81394f7.png">

Following the project pipeline below, the project is borkend down into a few sections.
![Capturesss](https://user-images.githubusercontent.com/48291391/61484669-61de5180-a96d-11e9-9851-fda95e4ef447.PNG)
```
  **1. Loading and visualizing the data.**  -- 80% used as trainig images; 20% used as testing images
  **2. Pre-processing.** The input images are standardized to be with the same size, and the output is implemented with an array of one-hot encoder labels.
  **3. Feature extraction.** The brightness feature of HSV is used to mask out 3 parts with equal area, top, middle and bottom where red, yellow and green light lie in correspondingly.  Then Maximum Average__Brightness is compared between these 3 areas to define what kind of light image it is.
  **4. Classification and visualizing error.** Using this method yield a good result with 99.3% pass (295 out of 297).
  **5. Evaluation.** The drawback of this method is that relies on where the light is in the image. In other words, this method assumes the locations of lights are where they're supposed to be. For instance, if the green light in the images is at the middle section so the bottom section has empty image, this method could not mask out the green color out in the bottom section.
```
## Example of the Results

![result1](https://user-images.githubusercontent.com/48291391/61486267-044c0400-a971-11e9-8952-87be8e80e201.PNG)
