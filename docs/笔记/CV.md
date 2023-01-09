> First version on 2022-6-18
>
>Last version on 2022-6-18
>
>Author :FeynmanRP

# CV
## Image Acquisition

### Aperture
![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618164149.png)

Why not make the aperture as small as possible?
* Less light gets through
* Diffraction effects

### Reason for lenses
* Focus all lights shed on the lens to a single point
* Much more energy efficient than a pinhole

### Thin lens equation
$$\frac{1}{d_o}+\frac{1}{d_i}=\frac{1}{f}$$

### Depth of Field 
![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618165105.png)


![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618165219.png)

Changing the aperture size affects depth of field 

* A smaller aperture increases the range in which the object is approximately in focus
* But small aperture reduces amount of light –need to increase exposure

#### F-number
* F-number:focal length / aperture diameter
* Aperture size is controlled by the F-number

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618170958.png)

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618171124.png)

Exposure: shutter speed vs. aperture
![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618171258.png)

### Field of View (Zoom)
FOV depends of Focal Length

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618171915.png)

Size of field of view governed by size of the camera retina:

$$\varphi=tan^{-1}\frac{d}{2f}$$

Smaller FOV = larger Focal 

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618172349.png)

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618172520.png)

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618173346.png)

### Lens Flaws: Chromatic Aberration

Color fringes near edges of image

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618172910.png)

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618173219.png)

Corrections:

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220618173052.png)

## Basic Concepts of Images
### Digital image acquisition
* Digital image acquisition
* Image sampling and quantization
  * Choose number of gray levels (according to number of assigned bits)
  * Divide continuous range of intensity values
  * Low freq. areas are more sensitive to quantization

* Digital image representation
  * Discrete gray levels:$L=2^k$
  * The number, b, of bits required to store a digitized image is:$b=M*N*k$
* Zoom in & Zoom out
* Relationships Between Pixels
  * The 4-neighbors of p
  * The 8-neighbors of p

### Format of Image File 

Lossy vs. Lossless compression

* A lossless compression algorithm discards no information 
* lossy algorithms accept some degradation in the image in order to achieve smaller file size

Image File Format

* RAW:An image output option available on some digital cameras. 
  * Pros:"lossless" format -allows full post processing of all in-camera variables (white balance, saturation, sharpness, etc.).
  * Cons:Proprietary camera manufacturer format (multiple standards), not all software can view RAW files, large file size. Not web browser compatible. 
* BMP:bitmap image fileordevice independent bitmap (DIB) file format.

  * Pros:"lossless" format –Good photo quality. 1-bit through 24-bit color depthWidely compatible with existing Windows programs, especially older programs
  * Cons:withoutcompression, which results in very large files Not supported by Web browsers 
* TIFF (Tagged Image File Format):TIFF has the option of being compressed, using a lossless compression technique known as LZW, which will shrink the image with no loss of data. 

  * Pros:Huge file size even when compressed, has multiple "standards" so not all programs can read all TIF files. Not web browser compatible
  * Cons:"lossless" format -all image information is retained. 
* GIF (Graphics Interchange Format ):Be compressed using the LZWlossless data compressiontechnique. 
  * Pros:
    * uses lossless compression
    * suitable for logos/icons, flat areas of color with well defined regions
    * support for transparency
    * suitable for small animations 
  * Cons:
    * the oldest format for web –1989
    * in most cases it has a bigger file size than PNG 
* PNG (Portable Network Graphics 1996):is the most used lossless image compression format on the Internet. 

  * Pros:
    * 24bit color / 8bit color(256 colors)
    * uses lossless compression
    * suitable for transparent or semitransparent images
    * in most cases PNG has a smaller file size than GIF
    * it has alpha channel transparency 
    * proposed as replacement of GIF by World Wide Web Consortium 
  * Cons:
    * it is wise to avoid using PNG with big photos and images with details because of the big generated file size
    * in different situations it has bigger file sizes than JPG 
* JPEG :The degree of compression can be adjusted, allowing a selectable tradeoff between storage size and image quality. JPEG typically achieves 10:1 compression with little perceptible loss in image quality.  
  * Pros:
    * 24bit color
    * suitable for images, high details & quality pictures
    * uses loss compression
    * used in design and photography industry –it is likely to see nature photos in JPG file format 
    * it is good when you are willing to drop quality from a picture for the sake of file size
  * Cons:
    * They tend to discard a lot of data
    * After compression, JPEG tends to create artifacts
    * Cannot be animated
    * Does not support transparency
### When should you use each?
* TIFF
  * the best quality output from a digital camera
  * as the working storage format as you edit and manipulate digital images
  * Do NOT use TIFF for web images 
* JPG
  * the format of choice for nearly all photographs on the web 
  * Digital cameras save in a JPG format by default 
  * Never use JPG for line art 
* GIF
  * If your image has fewer than 256 colors and contains large areas of uniform color, GIF is your choice. The files will be small yet perfect. 
  * DoNOTuse GIF for photographic images, since it can contain only 256 colors per image. 
* PNG
  * If you have an image with large areas of exactly uniform color, but contains more than 256 colors, PNG is your choice. Its strategy is similar to that of GIF, but it supports 16 million colors, not just 256. 
  * If you want to display a photographexactlywithout loss on the web, PNG is your choice. Later generation web browsers support PNG, and PNG is the only lossless format that web browsers support. 

## Images Enhancement

Problem Oriented
* Highlighting interesting detail in images
* Removing noise from images
* Making images more visually appealing
* De-emphasizingthings in an image
* Findingthings in an image

Categories of image enhancement approaches
* Spatial Domain Methods:The image plane itself. Direct manipulation of pixels in an image
* Frequency Domain Methods:Consider the image as a 2D signal and apply Fourier transformProcess the image in the transformed domainApply the inverse transform to return into the spatial domain

### Gray Level Transformations
#### Negative transformation

$$s=L-1-r$$

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220619162336.png)

#### Log transformation

$$s=c*log(1+r)$$

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220619162736.png)
#### Power-law (Gamma) transformations

$$s=c*r^{\gamma}$$

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220619162827.png)

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220619163020.png)

#### Piecewise Linear Transformation
![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220619164134.png)

### Histogram Processing
#### Global histogram equalization
![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220619164602.png)

#### Adaptive histogram equalization
![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220619165147.png)

### Arithmetic/Logical Operation
* Logic Operations
* Image Subtraction
* Image Averaging

### Spatial Filtering
#### Fundamentals
![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220619184732.png)

#### Smoothing
Smoothing linear spatial filters are used for blurring and / or for noise reduction

How big shouldthe mask be?The bigger the mask,
* more neighbors contribute.
* smaller noise variance of the output.
* bigger noise spread.
* more blurring.
* more expensive to compute.

#### Sharpening
**Properties of 1st and 2nd-Order Derivatives**

Conclusion:
* First-order derivatives generally produce thicker edges in an image
* Second-order derivatives have a stronger response to fine detail, such as thin lines and isolated points
* First order derivatives generally have a stronger response to a gray-level step
* Second-order derivatives produce a double response at step changes in gray level

**Use of 2nd Derivatives for Enhancement-The Laplacian**

A common second derivative sharpening filter is the Laplacian
![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220620000258.png)

The result of a Laplacian filtering is not an enhanced image
* We have to do more work
* Subtract the Laplacian result from the original image to Laplacian Filtered Image generate our final sharpened enhanced image

$$g(x,y)=f(x,y)-\nabla^2 f(x,y)$$

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220620000638.png)

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220620000814.png)

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220620000958.png)

**Use of 1st Derivatives for Enhancement -The Gradient**

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220620001409.png)

* Sobel gradient aids to eliminate constant or slowly varying shades of   gray and assist automatic inspection
* It also enhances small discontinuities in a flat gray filed

**Combing Spatial Enhancement Methods**

Utilize the Laplacianto highlight fine detail

Utilize the gradientto enhance prominent edges

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220620004101.png)

Combine Laplacian and smoothed gradient to get the detail-enhanced and noise-compressed image

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220620004149.png)

Combine Laplacian and smoothed gradient to get the detail-enhanced and noise-compressed image

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220620004221.png)

Increase the contrast of low gray levels by using a gray-level transformation

![](https://pic-imge.oss-cn-hangzhou.aliyuncs.com/img/20220620004244.png)

### Frequency Filtering

#### Fourier Transform and the Frequency Domain