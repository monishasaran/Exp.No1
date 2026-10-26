# Exp.No1 : Image Handling and Pixel Transformations using OpenCV Assignment
## AIM:
Write a Python program using OpenCV that performs the following tasks:

Read and Display an Image.
Adjust the brightness of an image.
Modify the image contrast.
Generate a third image using bitwise operations.
Software Required:
Anaconda - Python 3.7
Jupyter Notebook (for interactive development and execution)

## Algorithm:
Step 1:
Load an image from your local directory and display it.

Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.
Display the original, brighter, and darker images.

Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).
Display the original, lower contrast, and higher contrast images.

Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
Name: Monisha S

Register Number: 212225040258

## PROGRAM:
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('Moni.jpeg', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
image = cv2.imread('Moni.jpeg')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
image = cv2.imread('Qno. 1.jpg')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
image = cv2.imread('Moni.jpeg') 
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10) 
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
image = cv2.imread('Moni.jpeg') 
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
image = cv2.imread('Moni.jpeg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
image[200:500, 200:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
image = cv2.imread('Moni.jpeg')
image.shape
roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349
# Convert BGR to RGB for displaying with Matplotlib
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
# Display the cropped region (ROI)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
# Load the image
image = cv2.imread('Moni.jpeg')
# Flip the image horizontally (left-right)
flipped_horizontally = cv2.flip(image, 1)
# Convert BGR to RGB for displaying with Matplotlib
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
# Horizontal flip
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
# Flip the image vertically (up-down)
flipped_vertically = cv2.flip(image, 0)
# Convert BGR to RGB for displaying with Matplotlib
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
# Vertical flip
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

## OUTPUT:
<img width="362" height="488" alt="image" src="https://github.com/user-attachments/assets/1d2272c7-b50c-4b49-b38d-8a93c7c2fba0" /> <img width="367" height="505" alt="image" src="https://github.com/user-attachments/assets/c7133db0-dab9-4c2d-92bf-e91dd0b48adf" />
<img width="362" height="493" alt="image" src="https://github.com/user-attachments/assets/447abd81-b714-46a6-ae4d-6e505658d1ea" /><img width="368" height="497" alt="image" src="https://github.com/user-attachments/assets/3a6bcf56-96fe-41ba-bd97-1085400bf551" />
<img width="360" height="495" alt="image" src="https://github.com/user-attachments/assets/bb38c745-cb6d-4f75-928e-f4c77207e3f0" /><img width="360" height="492" alt="image" src="https://github.com/user-attachments/assets/ac30574e-f567-4ebd-9ee4-0ca47ea17151" />
<img width="357" height="487" alt="image" src="https://github.com/user-attachments/assets/016d0e13-fb67-4fc8-a850-da75c07cdd30" /><img width="356" height="495" alt="image" src="https://github.com/user-attachments/assets/9c8406e4-9a81-43a1-b3bc-e3294429a4b9" />
<img width="360" height="488" alt="image" src="https://github.com/user-attachments/assets/930613e2-7ef9-4376-8da5-c6d3d0ed482d" /><img width="362" height="492" alt="image" src="https://github.com/user-attachments/assets/2b4c3c1f-7f99-444b-bd53-31de686a754c" />
<img width="587" height="500" alt="image" src="https://github.com/user-attachments/assets/e6cf0c99-1ffa-4a13-8cfd-a3875a33ed23" /><img width="471" height="495" alt="image" src="https://github.com/user-attachments/assets/74bee189-f7c7-4109-b99b-11f01514a890" />
<img width="362" height="502" alt="image" src="https://github.com/user-attachments/assets/1d6c8808-34d7-4848-b1ae-3d6a6ea5c3e3" /><img width="360" height="493" alt="image" src="https://github.com/user-attachments/assets/b988d3b9-7c73-48fd-b280-eceeb6669c6b" />














## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.


