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

### Step6:

Rotate the image using angle function.

## Program:
```
Developed By: 
Register Number: 212222230103
```

## i)Image Translation

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("vijay.jpg")
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

## ii) Image Scaling

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("vijay.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```


## iii)Image shearing

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("vijay.jpg")
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


### iv)Image Reflection

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("vijay.jpg")
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


### v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("vijay.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()

angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(input_image,M,(int(cols),int(rows)))

plt.imshow(rotated_img)
plt.show()
```



### vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("vijay.jpg")
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

![image](https://github.com/user-attachments/assets/bd5090d3-f4e5-4c6f-ad64-5f8b2a157e6e)



### ii) Image Scaling

![image](https://github.com/user-attachments/assets/1bb59c06-f2be-4a8f-aba0-491c7ca3f8ae)


### iii)Image shearing
![image](https://github.com/user-attachments/assets/ce12658a-eba5-4791-99ca-33a83ea85a1b)
![image](https://github.com/user-attachments/assets/57612389-8254-44f8-bb9b-17c67f00283a)



### iv)Image Reflection

![image](https://github.com/user-attachments/assets/5118678a-07c2-4ee4-9dbf-d2e273dafdaf)
![image](https://github.com/user-attachments/assets/4be49a9b-3899-4bb3-b184-60202a611369)


### v)Image Rotation

![image](https://github.com/user-attachments/assets/74e29e9e-e6e9-46cc-9927-0d00e72c3ea9)


### vi)Image Cropping

![image](https://github.com/user-attachments/assets/edcee11e-456f-4020-ba6a-bf8e454758a4)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
