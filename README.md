# animation
animated canvas boilerplate

## usage
Instantiate an Animation object by passing in an HTML element that will contain the canvas, a method to callback each frame, a method to callback to render, and a size object (with the shape { width: 100, height: 100}) to indicate the aspect ratio of the canvas.

### animationCallback(elapsedTime)
This callback should accept as its only argument a value indicating how many milliseconds have passed since the last frame
The method should return true/false indicating whether the result of the frame requires a re-render

### render(htmlCanvas)
This callback accepts one argument: the canvas DOM element created by the Animation object. It is used to get a context and draw content (obviously)


#### known limitations
With the animationCallback only returning a blanked true/false, either the entire scene is re-rendered or none of it is. For many uses this is sufficient, however, more complex rendering sequences could benefit from an invalidating rectangles process.
