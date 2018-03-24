
##PROJECT WRITEUP

[image1]: ./examples/grayscale.jpg "Grayscale"

---
###The Pipeline
The work flow of the pipeline is fairly basic when it comes to handling computer vision.

Pass image location to function 

Read image data using 

Make copies of image so you do not manipulate original.

Process first copy by first converting it to grayscale.
Smooth it with a gaussian filter. This will reduce the gradients and remove the smaller less important gradients

Take 


###Shortcomings
Two shortcomings in regards to this build both happen within the draw_lines().

1. When the pipeline is processing video a couple of frames will drawn lines that are just off of the lines painted on the road.
This is definitely due to draw_lines(). Some of the filtering and calculation methods are unable to throw out bad slope calculations and find a more appropriate slope. It is a very calculation heavy function estimating slope, and the x points that will be drawn. 

I didn't want to use the same function that was given in the walkthrough video so I dug deep and built my own. From the looks of it the example method of calculating the slope and points creates a more reliable lines. But learned a lot about lines and manipulating data by building my own.


2. Currently cannot process the challenge video due to inability to throw out crazy slope calculations as mentioned earlier. 
draw_lines() does not handle bad slopes very well. When a filter is implemented to throw out bad slopes it ends up throwing all slopes. Not sure why logical operator is not handling good vs bad correctly. Need someone to bounce thoughts off of. Or spend a lot more time on this project than I have or was intended for this project.

###Next Iteration Improvements
1. Improve draw_lines() to handle issues mentioned above.
2. Figure out how to draw curved lines using functions other than point to point linear calculations.
