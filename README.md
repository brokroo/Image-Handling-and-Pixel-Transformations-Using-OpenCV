# Image-Handling-and-Pixel-Transformations-Using-OpenCV 

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
- **Name:** SANJITH R
- **Register Number:** 212223230191

  ### Ex. No. 01

### **Step 1: Read and Display Image**
```python
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('vr46.png', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb, cmap='viridis')  
plt.title("Original Image")
plt.axis('off')  
plt.show()
```
### **Step 2: Draw a Line**
```python
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```

### **Step 3: Draw a Circle**
```python
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

### **Step 4: Draw a Rectangle**
```python
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

### **Step 5: Add Text**
```python
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```

### **Step 6: Convert RGB to HSV**
```python
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```
### **Step 7: Convert RGB to Gray**
```python
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```
### **Step 8: Convert RGB to YCrCb**
```python
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```

### **Step 9: Convert HSV back to RGB**
```python
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```

### **Step 10: Modify Pixel Block**
```python
image[200:500, 200:500] = [255, 255, 255]
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```

### **Step 11: Resize Image**
```python
resized_image = cv2.resize(image, (768 // 2, 600 // 2))
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```

### **Step 12: Crop ROI**
```python
roi = image[50:350, 50:350]
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```

### **Step 13: Flip Horizontally**
```python
image = cv2.imread('vr46.png')
flipped_horizontally = cv2.flip(image, 1)
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```

### **Step 14: Flip Vertically**
```python
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

### **Step 15: Save Final Image**
```python
cv2.imwrite(
"final_output.jpg",
flipped_horizontally
)**
```

## Output:
### Original Image
<img width="4096" height="2731" alt="1338658" src="https://github.com/user-attachments/assets/e50b57f6-53fe-4b8e-826b-a428d2effed8" />

### Image with Circle

<img width="405" height="280" alt="image" src="https://github.com/user-attachments/assets/a149d408-0eb8-4ffa-8b0a-53d9d8358be9" />


### Image with Rectangle

<img width="435" height="290" alt="image" src="https://github.com/user-attachments/assets/c5302187-3f6d-45d7-b427-b66b40c5adf9" />

### Image with Text

<img width="506" height="357" alt="image" src="https://github.com/user-attachments/assets/5acab469-270c-4228-bbc6-9c58b9bb907d" />


### ORIGINAL, BRIGHTER and DARKER Images

<img width="531" height="377" alt="image" src="https://github.com/user-attachments/assets/b9e5fc16-e692-4a87-bfc2-24e00a6eb315" />


<img width="525" height="381" alt="image" src="https://github.com/user-attachments/assets/5de0f1ad-e63c-4367-8532-bd11ba84066c" />


<img width="532" height="388" alt="image" src="https://github.com/user-attachments/assets/3df5e6ef-29b7-4023-836d-f5db04cfe4ca" />




### Resized Image

<img width="260" height="343" alt="image" src="https://github.com/user-attachments/assets/efadd2d5-fae9-4c6f-b7a5-0220eca24d35" />


### Cropped ROI

<img width="377" height="381" alt="image" src="https://github.com/user-attachments/assets/84ce15af-6669-46b4-995a-d64dbf814e06" />

### Flipped Images

<img width="253" height="352" alt="image" src="https://github.com/user-attachments/assets/103daf22-7785-42ce-ac62-c9c8eeb7846a" />

### ORIGINAL AND SATURATED
<img width="940" height="337" alt="image" src="https://github.com/user-attachments/assets/ca70b627-0939-43d6-b37f-1108c29851e9" />

### HSV, Gray and YCrCb Images
<img width="902" height="187" alt="image" src="https://github.com/user-attachments/assets/d8c96d69-ea69-4640-a250-0874a4f8d17d" />

### ORIGINAL AND COLOR SATURATED
<img width="797" height="292" alt="image" src="https://github.com/user-attachments/assets/23095633-7eef-453b-a297-53c956936483" />

## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.

