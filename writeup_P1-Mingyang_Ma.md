# **Finding Lane Lines on the Road** 

## Mingyang Ma 

### Project 1-- 17.Jan.2019 
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

My pipeline consisted of 6 steps. 

1. convert orginal img to gray image 
2. use the GussianBlur to get blur image 
3. use Canny Algo to do Edge detection 
4. get the Range of interested Area 
5. use Hough Lines function from Opencv to detect straight lines
6. process the result of the Hough lines, filter, and get final results of the left and right lane lines. 
7. draw final lane lines in images

more details in commands in code. 

### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be by cerntain situation, many parameter in the functions should be fixed again. 

For example, the most commen issue I can imagine will be the minimal gap parameter in  Hough Lines. this could be change in a big range based on the 
quality not only of the image but also the quality of the roads/ lanes. 
So to set a exact number as the parameter does not seems to be the best solution. 



### 3. Suggest possible improvements to your pipeline

For overcome the parameter problem, I think it might be a solution to use flexible parameter based on a pre-decide/detect function, add into the
pipeline to tell the road/ lane or video quality situation. And then set a better parameter in each situation. 

