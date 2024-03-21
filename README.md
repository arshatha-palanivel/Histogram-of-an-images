# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:

### Developed By: ARSHATHA 
### Register Number: 212222230012

## Input Grayscale Image and Color Image:
```python
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('strawberries.jpg')
Color_image = cv2.imread('panda.jpeg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()
```

## Histogram of Grayscale Image and Green channel of Color Image:
```py
hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram of Color Image Green Channel")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

```

## Histogram Equalization of Grayscale Image:
```py
import cv2
gray_image = cv2.imread("strawberries.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/arshatha-palanivel/Histogram-of-an-images/assets/118682484/946c0c55-4e79-4279-8961-7d6526cdc7e3)

![image](https://github.com/arshatha-palanivel/Histogram-of-an-images/assets/118682484/ff271060-05a6-4858-acec-620215e2c312)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/arshatha-palanivel/Histogram-of-an-images/assets/118682484/42eb231b-3eb2-4207-a512-b5005105a51b)

![image](https://github.com/arshatha-palanivel/Histogram-of-an-images/assets/118682484/28c37562-2031-4953-96fd-9fd9c0a3dc98)


### Histogram Equalization of Grayscale Image.


![image](https://github.com/arshatha-palanivel/Histogram-of-an-images/assets/118682484/a1acb819-2941-4923-9dc6-7e44cd52e4a0)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
