# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary libraries.

### Step2:
Read the images using imread() function.

### Step3:
Using calcHist() we can find the histogram of the images.

### Step4:
Using equalizeHist() we can equalize the image.

### Step5:
Using matplotlib.pyplot plot the histogram.

## Program:
```
# Developed By: Thirukaalathessvarar S
# Register Number: 212222230161
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

gray_image = cv2.imread("dip4.jpg")
color_image = cv2.imread("dip4(2)",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Display the histogram of gray scale image and any one channel histogram from color image

grayscale_image=cv2.imread("dip4.jpg")
colourscale_image=cv2.imread("dip(2).jpg")
hist=cv2.calcHist(grayscale_image,[0],None,[255],[0,255])
hist1=cv2.calcHist(colourscale_image,[1],None,[255],[0,255])
plt.figure()
plt.title("Histogram")
plt.xlabel("grayscale")
plt.ylabel("pixel count")
plt.stem(hist)
plt.show()
plt.xlabel("colour scale")
plt.ylabel("pixel count")
plt.stem(hist1)
plt.show()


# Write the code to perform histogram equalization of the image. 

gi=cv2.imread("dip4.jpg",0)
colorscale=cv2.imread("dip4(2).jpg")
g=cv2.resize(gi,(500,400))
equ=cv2.equalizeHist(gi)
cv2.imshow("Grey Scale",g)
cv2.imshow("Equalization",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image

![gray_dip4](https://github.com/Thirukaalathessvarar-S/HISTOGRAM/assets/121166390/bd762b40-15e7-4e8e-820d-f74e4aea716a)

![dip4_riyal](https://github.com/Thirukaalathessvarar-S/HISTOGRAM/assets/121166390/80eab26a-54e0-4e0d-8fc8-1cf041b65599)

### Histogram of Grayscale Image and any channel of Color Image
![dip3_exp4](https://github.com/Thirukaalathessvarar-S/HISTOGRAM/assets/121166390/7793ff4e-c3ad-4262-a8d8-65467fb7b179)

![dip4_exp4](https://github.com/Thirukaalathessvarar-S/HISTOGRAM/assets/121166390/51490044-4111-4b67-b55c-6acdfee2d061)


### Histogram Equalization of Grayscale Image
![dip2_exp4](https://github.com/Thirukaalathessvarar-S/HISTOGRAM/assets/121166390/eb1e9f24-6c50-4d0a-924c-3215f5841f02)

![dip4_equalization](https://github.com/Thirukaalathessvarar-S/HISTOGRAM/assets/121166390/1496df35-5e36-4294-92c4-6649fecc3a17)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
