## Reading, writing and visualizing the images

#### in vscode make a folder named opencv which contains folder named data with image (abc.jpg)

### python code
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
```




## Read, write ans=d visualize videos

```python
import os
import cv2

`read`
video_path = os.path.join('.', 'data', 'dog.mp4')
video = cv2.VideoCapture(video_path)

`visualize`
ret = True
while ref:
     ret, frame = video.read()
     if ret:
         cv2.imshow('frame', frame)
         cv2.waitKey(40)
video.release()
cv2.destoryAllWindows()
```

## webcam

```python
import cv2

#read
webcam = cv2.VideoCapture(0)

 #visualize
while True:
    ret, frame = webcam.read()
    cv2.imshow('frame', frame)
    if cv2.waitKey(40) & 0xFF == ord('q'):
        break
webcam.release()
cv2.destroyAllWindows()
```



