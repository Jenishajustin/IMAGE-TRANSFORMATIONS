# IMAGE TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image.

### Step5:
Reflect of the image.

### Step6:
Rotate the image.

## Program:
```
Developed By: J.JENISHA
Register Number: 212222230056
```
```python
i) Original Image
# To show the original image and to find the shape of the image
import cv2
import numpy as np
img = cv2.imread('tan.jpg',-1)
re=cv2.resize(img,(400,300))
original = cv2.cvtColor(re , cv2.COLOR_BGR2RGB)
cv2.imshow('input',original)
cv2.waitKey(0)
cv2.destroyAllWindows()
original.shape
row, col, dim =original.shape

ii)Image Translation
translation = np.float32([[1,0,100],[0,1,150],[0,0,1]])
translated_image = cv2.warpPerspective(original,translation,(col,row))
cv2.imshow('translated_image',translated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

iii)Image shearing
shear_x = np.float32([[1,0.7,0],[0,1,0],[0,0,1]])
shear_y = np.float32([[1,0,0],[0.3,1,0],[0,0,1]])
sheared_x= cv2.warpPerspective(original,shear_x,(col,row))
sheared_y = cv2.warpPerspective(original,shear_y,(col,row))
cv2.imshow('shear_x',sheared_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('shear_y',sheared_y)
cv2.waitKey(0)
cv2.destroyAllWindows()

iv)Image Reflection
ref_x = np.float32([[1,0,0],[0,-1,row],[0,0,1]])
ref_y = np.float32([[-1,0,col],[0,1,0],[0,0,1]])
reflect_x= cv2.warpPerspective(original,ref_x,(col,row))
reflect_y = cv2.warpPerspective(original,ref_y,(col,row))
cv2.imshow('reflected_x',reflect_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('reflected_y',reflect_y)
cv2.waitKey(0)
cv2.destroyAllWindows()

v)Image Rotation
angle = np.radians(15)
mat_rotate = np.float32([[np.cos(angle),-
(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotate_img =cv2.warpPerspective(original,mat_rotate,(col,row))
cv2.imshow('rotated',rotate_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

vi)Image Cropping
cropped_img=img[10:500,25:600] 
cv2.imshow('after_cropping',cropped_img);
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Original image
![Screenshot 2024-04-12 111311](https://github.com/Jenishajustin/IMAGE-TRANSFORMATIONS/assets/119405070/f5406c6c-0f22-453e-a05b-1844b6ebe3f4)

### i)Image Translation
![Screenshot 2024-04-12 111440](https://github.com/Jenishajustin/IMAGE-TRANSFORMATIONS/assets/119405070/7828d535-878d-4475-9c8d-6548af16e282)

### ii)Image shearing
![Screenshot 2024-04-12 111551](https://github.com/Jenishajustin/IMAGE-TRANSFORMATIONS/assets/119405070/e1005064-f047-4d4f-980c-cfce9e18000b)

![Screenshot 2024-04-12 111603](https://github.com/Jenishajustin/IMAGE-TRANSFORMATIONS/assets/119405070/affdf3af-b6cd-412a-9cdb-b0ab076a0532)

### iii)Image Reflection
![Screenshot 2024-04-12 111710](https://github.com/Jenishajustin/IMAGE-TRANSFORMATIONS/assets/119405070/e768c15b-b71d-4049-bd24-c67efac25db0)

![Screenshot 2024-04-12 111721](https://github.com/Jenishajustin/IMAGE-TRANSFORMATIONS/assets/119405070/edbcf1a1-802f-42a6-8ec9-f705e302cad0)

### iv)Image Rotation
![Screenshot 2024-04-12 111808](https://github.com/Jenishajustin/IMAGE-TRANSFORMATIONS/assets/119405070/b2c39eb8-660b-417e-ac28-a362c29d8dc2)

### v)Image Cropping
<img src="https://github.com/Jenishajustin/IMAGE-TRANSFORMATIONS/assets/119405070/4125076c-9a24-469d-ae78-ad1b88b36f20" height=450 with=250>

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
