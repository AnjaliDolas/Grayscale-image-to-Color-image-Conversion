# Grayscale-image-to-Color-image-Conversion

**Problem statement**
Colorization of grayscale images in order to enhance their visual appeal of Forest images came from Satellite using Pseudo Coloring

**What is Pseudo Coloring?**
* Pseudo coloring is a process of assigning colors to gray values of a grayscale image, based on a specified criterion.
* By using the color assignment, a grayscale image is converted into Pseudo Color image

**Why Pseudo Coloring?**
* The principal use of pseudo coloring is to make a grayscale image better for human visualization and interpretation.
* As it is the fact that humans can discern thousands of color shades and intensities, compared to less than two dozen shades of gray.

**Technical specifications**
* Grayscale image: It is a black and white image. The pixels values are shades of gray color which is the combination of white and black shades. The image is 
represented in form of one 2-Dimensional matrix. Each value represents the intensity or brightness of the corresponding pixel at that coordinate in the image. 
Total 256 shades are possible for the grayscale images. 0 means black and 255 means white. As we increase the value from 0 to 255, the white component gets 
increases and brightness increases.

* RGB color image: It is a colored image. It consists of three 2-Dimensional matrices, which are called channels. Red, Green and Blue channels contain the 
corresponding color values for each pixel in the image. In integer format, the range of pixel intensity goes from 0 to 255. 0 means black and 255 represents the 
highest intensity of the primary color. There exist 256 shades of each color.

** 1. Pseudo Coloring using "Intensity Slicing"**
* The technique of intensity slicing and color coding is the simplest example of pseudo-coloring of grayscale digital images.

![image](https://github.com/AnjaliDolas/-Grayscale-image-to-Color-image-Conversion/assets/104906262/2ec25e31-bb1a-457d-a91c-135c96164156)

* In this scheme, a group of intensities (Slice of grayscale image) is assigned a particular color of choice as shown in figure below.
* The suggested scheme is suitable when number of selected colors are less. Less numbers of colors (Slices) create color images having abrupt changes in colors. 
One such example is shown below. This uses 5 different colors.
  
![image](https://github.com/AnjaliDolas/-Grayscale-image-to-Color-image-Conversion/assets/104906262/1fbaa3eb-a644-49ec-b724-9ae8968db65c)

![image](https://github.com/AnjaliDolas/-Grayscale-image-to-Color-image-Conversion/assets/104906262/cb3360a9-2d6a-4b6e-bdea-3c55d047f6a9)

![image](https://github.com/AnjaliDolas/-Grayscale-image-to-Color-image-Conversion/assets/104906262/64509f10-08fe-4d29-8f17-a86b80cdab3c)

* This scheme can be extended to assign 256 different colors to 256 gray levels of input image. This will create smooth transition of colors as shown below.

![image](https://github.com/AnjaliDolas/-Grayscale-image-to-Color-image-Conversion/assets/104906262/8c026bd7-6efc-4881-a3ed-8403b4de77d6)

![image](https://github.com/AnjaliDolas/-Grayscale-image-to-Color-image-Conversion/assets/104906262/c28798f2-948c-4f56-8a49-f57ad0735ff4)

**2. Pseudo Coloring using "Color Transformation"**
* Color Transformation based technique is more general, and thus is capable of achieving a wider range of pseudo color enhancement results than color slicing technique.
* The idea underlying this approach is to perform three independent transformations on the input intensities of grayscale image.
* The three outcomes of these transformations are clubbed together to create color image.
* This color content of output image depend on the nature of the transformation functions.

![image](https://github.com/AnjaliDolas/-Grayscale-image-to-Color-image-Conversion/assets/104906262/2e040f61-1f9a-4892-ac62-3706337dccc7)

**Literature survey **
There are mainly three types of pseudo-color transformations
1. Gray-level-based methods need to construct transform functions which convert gray values, gradients, or other gray-scale features into different colors. Such methods translate all gray levels into a set of colors based on a fixed rule without considering any contextual information. Hence, they overlook local details and yield roughly 
separate color images. 
2. Color-space-model-based methods, however, do not only rely on gray levels, but also rely on saturation, brightness, and other properties depending on color spaces. These methods overrate the roles of color spaces while underestimate intrinsical 
features that are essential to represent objects. Thus, they cannot provide color images of high resolution when color spaces fail to describe distinguish features of images. 
3. Frequency-based methods, using Fourier and wavelet transforms, construct transformations which convert features of frequency into colors. Since frequency is unable to represent all information dividually, such methods may fail in many cases.
Hence we are using Gray-level-based method for pseudo-color transformations.In Gray-level-based method we have choose the “Intensity slicing method”, because in that we can create our own colormap according to the need of the application.

For that “colormapeditor” is the function present in matlab.

**Colormap Editor Description**
* The Colormap Editor allows you to customize the colormap of the selected figure or axes.
Using the Colormap Editor, you can:
1. Choose a predefined colormap.
2. Import a saved colormap from the workspace.
3. Adjust the position of colors in the colormap.
4. Change the color at a specific position.

![image](https://github.com/AnjaliDolas/-Grayscale-image-to-Color-image-Conversion/assets/104906262/3ec04296-3181-4398-9ede-03a18c3fb9eb)
