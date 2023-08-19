
<p align="center"> <img src="https://jdleongomez.info/es/post/obs/featured.png" height="100" /> </p>

 # <p align="center">  You came too early, I haven't finished it yet </p>

---
<br>

# Table of Contents :books:
* Effect Filters
  * Color Correction
  * Chroma Key
 
* Audio Filters
  * Gain
   * Noise Gate
   * VST 2.x
 
 # Color Correction 🥀
  To understand this filter you must first understand how video capture works, when OBS captures a source, such as the game or the full screen, it obtains a sequence of images composed of pixels. Each pixel has three components red, green and blue, represented by numerical values usually 0 to 255 (if working in the RGB 8bit color space) these RGB channel values define the color and intensity of each pixel in the image, the value 0 represents the total absence of color while 255 indicates the maximum intensity of this color. When the scene is captured by OBS, the RGB values are stored in a matrix, where each element of the matrix represents a pixel and contains the values of its three channels, this pixel matrix is essentially a representation of the captured image OBS processes this matrix to display the image in real time or save it to a file.

  Within this matrix each row represents a row of pixels in the image and each column represents a pixel in that row, if you have a 1920x1080 image you would have a matrix of 1920 rows and 1080 columns. Now going a little deeper into this filter added in 2015 when applying this filter some specific mathematical calculations are performed on the values of the RGB channels of each pixel, these usually use a multiplication to the values of these channels, an example of this operation is the one seen in this image
<details><summary><b><h3>Image demonstrating mathematical calculations 🖼 </h3></b></summary>
 
Considering this, the pixel (5,10) had a previous value of `R = 150` `G = 135` `B = 8`, after applying the saturation taking into account that the intensity of the pixel is `97` the values are now `R = 144` `G = 131` `B = 16`, if we have a resolution in the OBS of 1920x1080 where there are 207363600 pixels, this procedure is done in each of the pixels.

  <img id="image" src="multimedia/1.png"> <br>
  <p align="center"> ❗ <b>The values were rounded up as some of them gave too many decimals, this was done to make the demonstration more understandable, in the real process the numbers are not rounded.</b> ❗ </p>
