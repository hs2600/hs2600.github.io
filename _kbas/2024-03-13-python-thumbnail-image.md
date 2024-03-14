---
layout: post
title: How to create image thumbnails with Python
date:   2024-03-13 00:00:00 -0800
description:
author: horacio 
image:  '/images/python.png'
tags:   [kba, technology]
tags_color: '#477690'
---

### The `PIL` library

[Python Imaging Library](https://pillow.readthedocs.io/en/latest/index.html){:target="_blank"} or `PIL` is an image processing library in python. This library supports a wide range of file formats, is designed for an efficient internal representation of image data, and provides powerful image processing capabilities.

Install Pillow with pip:

```python
python3 -m pip install --upgrade pip
python3 -m pip install --upgrade Pillow
```

### The `Image` module

The [Image](https://pillow.readthedocs.io/en/latest/reference/Image.html){:target="_blank"} module provides a class with the same name which is used to represent a `PIL` image. The module also provides a number of factory functions, including functions to load images from files, and to create new images.

### Code Example

The following script loads an image, rotates it 45 degrees, and displays it using an external viewer (usually xv on Unix, and the Paint program on Windows).

```python
from PIL import Image
with Image.open("hopper.jpg") as im:
    im.rotate(45).show()
```

### The `thumbnail` function

The `thumbnail` function is used to generate the thumbnail version of the given image no larger than itself. This method determines an acceptable thumbnail size to retain the image’s aspect ratio. 

### Syntax

```python 
Image.thumbnail(size)
```

### Code example

The following script creates a thumbnail of a single image.

```python
from PIL import Image
img = Image.open("image.jpg")

SIZE = (75, 75)

img.thumbnail(SIZE)

img.save('thumbnails/image.png')
```

## Create thumbnails

### Version 1

The following script creates thumbnails of all JPG images in the current directory preserving aspect ratios with 128x128 max resolution.

```python
from PIL import Image
import glob, os

size = 128, 128

for infile in glob.glob("*.jpg"):
    file, ext = os.path.splitext(infile)
    with Image.open(infile) as im:
        im.thumbnail(size)
        im.save("thumbnails/" + file + ".jpg", "JPEG")
```

### Version 2

Another version of a thumbnail generator script using images in current directory. This script uses a custom image resize function `resize_image`. The function will create a thumbnail with 300x300 max resolution.

```python
from PIL import Image
import glob, os

# define custom function
def resize_image(image, thumbnail_path):
    MAX_SIZE = (300, 300)
    with Image.open(image) as image:
        image.thumbnail(MAX_SIZE)
        image.save(thumbnail_path)

# load all images in current directory with specific extension 
for infile in glob.glob("*.jpg"):
    file, ext = os.path.splitext(infile)
    # Generate thumbnail
    thumbnail_path = "thumbnails/{}{}".format(file, ext)
    resize_image(infile, thumbnail_path)
```
