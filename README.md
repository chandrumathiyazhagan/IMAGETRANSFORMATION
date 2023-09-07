# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
## Step1:
Import the necessary libraries and read the original image and save it as a image variable.

## Step2:
Translate the image.

## Step3:
Scale the image.

## Step4:
Shear the image.

## Step5:
Find reflection of image.

## step6:
Rotate the image.

## Step7:
Crop the image.

## Step8:
Display all the Transformed images.

## Program:
```python
Developed By:M.CHANDRU
Register Number:212222230026
```
```python
i)Image Translation:

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image = cv2.warpPerspective(lion_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
```python
ii) Image Scaling:

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
scaled_img = cv2.warpPerspective(lion_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```
```python
iii)Image shearing:

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```
```python
iv)Image Reflection:

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
dog_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(lion_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(lion_image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```
```python
v)Image Rotation:

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(lion_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
```python
vi)Image Cropping:

import numpy as np
import cv2
import matplotlib.pyplot as plt
lion_image = cv2.imread("lion.jpeg")
lion_image = cv2.cvtColor(lion_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
cropped_img=lion_image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
![Screenshot from 2023-09-07 10-41-36](https://github.com/chandrumathiyazhagan/IMAGETRANSFORMATION/assets/119393023/46e05bcc-57f4-4a5b-a569-869793ed36bc)

### ii) Image Scaling
![Screenshot from 2023-09-07 10-44-07](https://github.com/chandrumathiyazhagan/IMAGETRANSFORMATION/assets/119393023/e3dbc21f-36a6-4438-8bbb-95d265b2f28f)

### iii)Image shearing
![Screenshot from 2023-09-07 10-47-47](https://github.com/chandrumathiyazhagan/IMAGETRANSFORMATION/assets/119393023/a5d89eda-d76b-4c6b-bad7-70d792f249ec)

### iv)Image Reflection
![Screenshot from 2023-09-07 10-50-52](https://github.com/chandrumathiyazhagan/IMAGETRANSFORMATION/assets/119393023/fb6a0da7-533a-4531-b706-5815d046dea8)

### v)Image Rotation
![Screenshot from 2023-09-07 10-52-54](https://github.com/chandrumathiyazhagan/IMAGETRANSFORMATION/assets/119393023/a18702bf-1d65-4148-94f8-0e85c7538344)

### vi)Image Cropping
![Screenshot from 2023-09-07 11-11-49](https://github.com/chandrumathiyazhagan/IMAGETRANSFORMATION/assets/119393023/973013e6-5595-4e92-9eea-fc70be1156df)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
