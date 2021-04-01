# RubiksCubeEncrypt-Image
Python3 Image encryption based on Rubik's Cube Principle

[Implementation of image cryptographic techniques](#https://www.hindawi.com/journals/jece/2012/173931/)
https://www.hindawi.com/journals/jece/2012/173931/

## requirement
```shell
pip3 install numpy
pip3 install opencv-python
```

## example how to use 
[example](example.ipynb)
```python3
import cv2

from src import encrypt as enc
from src import decrypt as dec
from src import genKey as gk

keyList = gk.gen_key(img, 1)

img = cv2.imread('image/bishil06.jpg')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

// encrypt
enc_img = enc.encrypt(img_rgb, keyList)

// decrypt
dec_img = dec.decrypt(enc_img, keyList)
```