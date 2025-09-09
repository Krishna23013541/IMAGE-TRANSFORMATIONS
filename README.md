# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import all the necessary modules

### Step2:
<br>
Choose an image and save it as filename.jpg

### Step3:
<br>
Use imread to read the image

### Step4:
<br>
Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

### Step5:
<br>
Use cv2.warpPerspective(image,M,(cols2,rows2)) to scale the image

### Step6:
Use cv2.warpPerspective(image,M,(int(cols1.5),int(rows1.5))) for x and y axis to shear the image

### Step7:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image

### Step8:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image

### Step9:
Crop the image to remove unwanted areas from an image

### Step10:
Use cv2.imshow to show the image

### Step11:
End the program

## Program:

Developed By: KRISHNA KUMAR R
Register Number: 212223230107

i)Image Translation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread("img0.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
print("Image Translation:")
plt.imshow(translated_image)
plt.show()

```
ii) Image Scaling
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('img0.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
print("Image Scaling:")
plt.imshow(translated_image)
plt.show()
```


iii)Image shearing
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('img0.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
print("Image Shearing:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```



iv)Image Reflection
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('img0.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```



v)Image Rotation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('img0.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Rotation:")
plt.imshow(translated_image)
plt.show()
```



vi)Image Cropping
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("img0.jpg")
h, w, _ = image.shape
cropped_face = image[int(h*0.2):int(h*0.8), int(w*0.3):int(w*0.7)]
cv2.imwrite("cropped_pigeon_face.jpg", cropped_face)
plt.imshow(cv2.cvtColor(cropped_face, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()
```

### Output:
### i)Image Translation
<img width="674" height="473" alt="image" src="https://github.com/user-attachments/assets/7795b3fa-f698-4a88-b851-4e068084b926" />


### ii) Image Scaling
<img width="689" height="217" alt="image" src="https://github.com/user-attachments/assets/5089f55f-74a0-4f0b-a4b4-5648da48302c" />


### iii)Image shearing
<img width="691" height="476" alt="image" src="https://github.com/user-attachments/assets/8e67a63d-9093-46de-af24-dfcf576d6945" />


### iv)Image Reflection

<img width="702" height="476" alt="image" src="https://github.com/user-attachments/assets/f101a262-8600-4a1a-8afc-2b23796ad4af" />


### v)Image Rotation

<img width="739" height="476" alt="image" src="https://github.com/user-attachments/assets/49da9eb7-ffad-4149-a7e6-9494380beb36" />


### vi)Image Cropping

<img width="703" height="512" alt="image" src="https://github.com/user-attachments/assets/0ff813c6-a9a3-4152-930d-48c313d6a415" />


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
