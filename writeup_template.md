# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps.
1) We Read our Image in a grey scale fromat
2) we do smoothing before applying canny algorithm by using Kernel size of 3
3) Apply Canny Detection with a low threshold 1 : 3 to high threshold 
4) Determine Region of interest to detect Lane lines in Image
5) using hough transfrom to find lines
6) separate line segments into left lines and right lines
    For each line:
     we calculate average slope and intercept
7) calculate x_min and x_max values using intercept, slope, y_min and y_max


### 2. Identify potential shortcomings with your current pipeline

I have a problem with calculating vertices, Need some smart implementation to calculate it without putting it hard coded

### 3. Suggest possible improvements to your pipeline

A possible improvement would be to write a function to calculate Vertices parames instead of putting it as hard coded values that depend on the data

