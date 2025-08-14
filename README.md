# Reading, writing and visualizing the images

### in vscode make a folder named opencv which contains folder named data with image (abc.jpg)

## python code
`pip install opencv-python`

```python
import os
import cv2

`read`
image_path = os.path.join('.', 'data', 'abc.jpg') `specified the path`
img = cv2.imread(image_path)

`write`
cv2 = cv2.imwrite(os.path.join ('.', 'data', 'abc_out.jpg'), img)

`visualize`
cv2.imshow('image', img)
cv2.waitKey(0)

