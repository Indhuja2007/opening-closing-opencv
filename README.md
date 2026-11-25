# Opening and Closing Operations Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological Opening and Closing operations on an image.

The program performs the following operations:

- Morphological Opening
- Morphological Closing

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create or load an input image containing foreground objects.

### Step 3:

Display the original image.

### Step 4:

Create a structuring element (kernel) of suitable size.

### Step 5: Opening Operation

- Apply the Opening operation using the structuring element.
- Opening consists of Erosion followed by Dilation.
- Remove small foreground noises while preserving the shape of larger objects.
- Display the opened image.

### Step 6: Closing Operation

- Apply the Closing operation using the structuring element.
- Closing consists of Dilation followed by Erosion.
- Fill small holes and gaps within foreground objects.
- Display the closed image.

### Step 7:

Compare the original, opened, and closed images.


## Developed By

**Name:INDHUJA.K**

**Register No:212225040133** 


## Program

### Original Image

```
img = cv2.imread("flower.jpg")

img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

plt.imshow(img_rgb)
plt.title("Original Image")
plt.axis("off")
plt.show()
```


### Opening Operation

```
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, kernel)

opening_rgb = cv2.cvtColor(opening, cv2.COLOR_BGR2RGB)

plt.imshow(opening_rgb)
plt.title("Opening Image")
plt.axis("off")
plt.show()
```

### Closing Operation

```
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, kernel)

closing_rgb = cv2.cvtColor(closing, cv2.COLOR_BGR2RGB)

plt.imshow(closing_rgb)
plt.title("Closing Image")
plt.axis("off")
plt.show()
```

### Display All Images Together

```
plt.figure(figsize=(15,5))

plt.subplot(1,3,1)
plt.imshow(img_rgb)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1,3,2)
plt.imshow(opening_rgb)
plt.title("Opening Image")
plt.axis("off")

plt.subplot(1,3,3)
plt.imshow(closing_rgb)
plt.title("Closing Image")
plt.axis("off")

plt.show()
```


## Output

### Original Image

- The input image is displayed.
- The image serves as the source for morphological processing.

<img width="487" height="507" alt="image" src="https://github.com/user-attachments/assets/48b79852-c34f-4d69-b431-5fdc0a448741" />


### Opening Operation

- Original image is displayed.
- Opened image is displayed.
- Small foreground noise is removed.
- Thin protrusions and isolated pixels are eliminated.
- Object boundaries become smoother.

<img width="480" height="500" alt="image" src="https://github.com/user-attachments/assets/7c35aaab-a9c2-457f-a86e-c5df070e85a1" />

### Closing Operation

- Original image is displayed.
- Closed image is displayed.
- Small holes and gaps inside objects are filled.
- Broken regions are connected.
- Object boundaries become more continuous.

<img width="480" height="502" alt="image" src="https://github.com/user-attachments/assets/f9564b64-cb40-40c1-a0c4-3e2e184fd383" />

### Display All Images Together

<img width="1360" height="437" alt="image" src="https://github.com/user-attachments/assets/a5ece811-c4c7-4e51-9213-0bfc0d3a8e8d" />

## Applications

### Opening

- Noise removal in binary images.
- Separation of connected objects.
- Preprocessing for object detection.

### Closing

- Filling small holes in objects.
- Connecting nearby components.
- Enhancing segmented regions.

## Advantages

### Opening

- Removes unwanted foreground noise.
- Preserves major object structures.
- Improves segmentation quality.

### Closing

- Restores object continuity.
- Eliminates small background gaps.
- Improves object representation.

## Result

Thus, the morphological operations **Opening** and **Closing** are successfully implemented using OpenCV. 
