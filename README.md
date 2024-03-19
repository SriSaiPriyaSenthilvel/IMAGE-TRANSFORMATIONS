# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.
<br>

### Step2:
Translate the image using a function warpPerpective()
<br>

### Step3:
Scale the image by multiplying the rows and columns with a float value.
<br>

### Step4:
Shear the image in both the rows and columns.
<br>

### Step5:
Find the reflection of the image.
<br>

### Step6:
Rotate the image using angle function.
<br>

## Program:
```python
Developed By: SRI SAI PRIYA.S
Register Number: 212222240103
i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\book.jpg')
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
ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\book.jpg')
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```
iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\book.jpg')
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
iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\book.jpg')
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
v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\book.jpg')
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
vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\book.jpg')
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```
```
## Output:
### i)Image Translation

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/2b69d98d-6393-4796-821d-72138b2ef4b8)

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/5d2d6f3d-39c3-4c31-adba-6d65504ecf89)

<br>

### ii) Image Scaling

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/e48502db-7b50-45aa-9ec3-3653a6623c46)

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/73c50eca-59ae-4218-8f71-70a63c26495a)

<br>
<br>


### iii)Image shearing

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/54da38bb-b6e6-4149-92e1-64572eafe5b9)

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/a779967c-69a6-406e-9728-6dd752bc7cb2)

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/3ef40b24-e80b-400e-abae-758c97853375)

<br>
<br>


### iv)Image Reflection

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/b2e1405d-6f81-4f53-ae8d-a9782f7d9db4)

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/b29d1f42-2a3f-44d2-a44b-0f740ebb63dc)

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/6a127e31-282e-4a7d-9478-17d45e67fdde)

<br>
<br>



### v)Image Rotation

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/c0c77fec-d8ec-4b49-917f-62282dbb9732)

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/1ff3113a-d702-4de5-9464-87a584608940)

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/539c906b-180c-44a5-8fe6-292a41abef5f)

<br>
<br>



### vi)Image Cropping

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/35e50943-e0b9-4870-a74f-68852d252d28)

![image](https://github.com/SriSaiPriyaSenthilvel/IMAGE-TRANSFORMATIONS/assets/119475702/8545f58e-d431-4438-8201-8095ccf085ec)

<br>
<br>

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
