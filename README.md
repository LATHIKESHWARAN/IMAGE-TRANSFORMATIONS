# IMAGE-TRANSFORMATIONS

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.
### Step2:
Translate the image using a function warpPerpective()
### Step3:
Scale the image by multiplying the rows and columns with a float value.
### Step4:
Shear the image in both the rows and columns.
### Step5:
Find the reflection of the image.
## Step 6:
Rotate the image using angle function.
## Program:
Developed By:LATHIKESHWARAN J
Register Number:212222230072
## Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("flor.jpeg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

##  Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("flor.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```
## Image shearing
```python 
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("flor.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```
## Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("flor.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
## Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("flor.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
## Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("flor.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation
![image](https://github.com/LATHIKESHWARAN/IMAGE-TRANSFORMATIONS/assets/119393556/87acbbe4-4635-49c7-89a0-5944edcd4194)


### ii) Image Scaling
![image](https://github.com/LATHIKESHWARAN/IMAGE-TRANSFORMATIONS/assets/119393556/ca2a003b-ce18-4d98-8698-5c2829b64eb2)


### iii)Image shearing
![image](https://github.com/LATHIKESHWARAN/IMAGE-TRANSFORMATIONS/assets/119393556/8a2fa91d-d19a-458d-89b0-a4b794b1bc15)

![image](https://github.com/LATHIKESHWARAN/IMAGE-TRANSFORMATIONS/assets/119393556/273c50c2-44c7-477d-823f-44a9b242c54f)


### iv)Image Reflection
![image](https://github.com/LATHIKESHWARAN/IMAGE-TRANSFORMATIONS/assets/119393556/15a85138-9e22-4b8b-922a-7621f4eef24f)

![image](https://github.com/LATHIKESHWARAN/IMAGE-TRANSFORMATIONS/assets/119393556/c92e0eb0-599f-4883-ade9-2c4ff8a189d1)


### v)Image Rotation
![image](https://github.com/LATHIKESHWARAN/IMAGE-TRANSFORMATIONS/assets/119393556/6f265e82-6454-4dd1-8bce-a75715a320b5)

![image](https://github.com/LATHIKESHWARAN/IMAGE-TRANSFORMATIONS/assets/119393556/eb2cad5b-205d-42e7-b24d-08efbbf5bb64)



### vi)Image Cropping
![image](https://github.com/LATHIKESHWARAN/IMAGE-TRANSFORMATIONS/assets/119393556/544a74e2-8afd-4127-9225-4cbe6330cce1)


## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
