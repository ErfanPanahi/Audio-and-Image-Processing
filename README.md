
# Audio-and-Image-Processing
In the image processing section of this repository, I address noise reduction using MATLAB's Fdatool and echo cancellation through Cepstrum transformation. Additionally, within the image processing domain, I explore solutions for enhancing image quality, ultimately culminating in the concept of scanning a paper sheet.

The completed sections of the project are as follows: (CA3_Matlab_810198369.mlx)

**1- Audio Signal Processing**

In this section, the process of echo and noise removal is examined using various filters.

a. Single Echo Filter

b. Noise Reduction Using FIR Filters (fdatool)

**2- Image Processing**

The process of image processing refers to a set of methods in which improving the quality of an image is addressed, or desired features are extracted from the image. In essence, image processing involves mapping from a space of m × n dimensions or m × n × 3 dimensions (depending on whether the image is grayscale or color) to another space. The dimensionality of this mapping's output, whether it remains an image or becomes features, can vary; in the case of the output still being an image, it would have dimensions of m × n, whereas if it becomes features, it could have different dimensions.

As we know, a black and white image is constructed from a matrix in which the elements inside represent the image's grayscale levels. If the image is in color, we require 3 matrices, each of which covers the primary colors, and with their values, the color of each pixel can be distinguished.

![image](https://github.com/ErfanPanahi/Audio-and-Image-Signal-Processing/assets/107314081/63622983-c943-4464-bc0c-13a859952e5f)

The kernel matrix is generally square and by applying it to images, the image quality can be improved or the desired use of the output can be achieved. Applying it to images refers to sliding it over the matrix of an image, or in other words, convolving it in a two-dimensional manner within the matrix of an image.

![image](https://github.com/ErfanPanahi/Audio-and-Image-Signal-Processing/assets/107314081/9c0f4f69-7e0b-4fec-842e-ce896ded426f)

![image](https://github.com/ErfanPanahi/Audio-and-Image-Signal-Processing/assets/107314081/4bbc6892-e973-4bc1-a7a6-043127fc6da2)

The output of applying each kernel to the image "house.jpg":

![image](https://github.com/ErfanPanahi/Audio-and-Image-Signal-Processing/assets/107314081/1d0e265e-b9d3-45ef-bf77-30c61e89e134)

**Defining the edges of the paper idea:**

First, we detect the edges of the paper using H-line and V-line kernels. 
![image](https://github.com/ErfanPanahi/Audio-and-Image-Signal-Processing/assets/107314081/99453278-aa77-499d-8468-f1196327dbbd)

As can be seen, the horizontal and vertical edges are indicated by these two white-colored filters. As demonstrated in computer exercise 2, white points have larger values, and therefore, we can conclude that if we sum the rows and columns, the white edges possess the highest values. Consequently, we can obtain the two horizontal edges and two vertical edges in the same manner. The intersection point of these 4 edges gives us the 4 corner points of the paper. Ultimately, by locating these 4 points and utilizing the `rectangle` command, we draw the rectangles of the edges of the image.



![image](https://github.com/ErfanPanahi/Audio-and-Image-Signal-Processing/assets/107314081/1eec4672-2424-4f57-a098-18bc544df0bf)

Finally, we also use another image to test the written function. (function is in live script (.mlx) file)
![image](https://github.com/ErfanPanahi/Audio-and-Image-Signal-Processing/assets/107314081/5eeb25af-fa4e-418f-857b-2a634cc924cf)

