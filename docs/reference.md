## Input Fields
Input fields control settings for how images are created and displayed.

### Top, Bottom, Left
These three fields allow you to define the area of the Mandelbrot set to display. After updating these fields, press the Draw button to update the image. The right edge is calculated based on a 3:4 (height:width) ratio.

### Color Palette Size
The palette size determines the maximum number of iterations used to determine if a point is in the Mandelbrot set. It also defines the length of `cmap`, the color map, where element *n* is the color to assign to points which escape the Mandelbrot set at iteration *n*.
A palette size of 256 will run faster that 1024, but will have fewer possible colors. 

### Precision
Precision is the `⎕FR` setting to use when calculating whether a point is in the Mandelbrot set. 1287 is much higher precision than 645 and allows for deeper zooming albeit at lower performance.

### Isolate Processes to Use
The explorer can use [isolates](https://docs.dyalog.com/20.0/files/Parallel_Language_Features.pdf) to distribute the computation load across multiple Dyalog APL processes. A setting of 0 means that isolates will not be used and all computation will be done in the current process. The initial value is set to 2 times the number of processors on your machine - this will help minimize any wait time for a processor.

### Zoom Level
Zoom Level is the factor by which the set will be zoomed in when you right-click the mouse on a point in the image.

### Slider Bar
The slider bar controls the delay between updates when the Colorize button is clicked. The delay ranges from 2 seconds to 0.1 seconds.

## Buttons

### Draw
The Draw button will redraw, but not recompute, the current image. This is useful when manually manipulating the color map `cmap`. See [Color Map](./colormap.md).

### Edit
Opens the [Color Map Editor](./colormap.md).

### Save
Allows you to have the current image as a .png file.

### Reset
Resets the image to the original set and color map.

### Quit
Quits (duh!)

### Help
Opens the Mandelbrot Explorer documentation.

### Colorize
Starts (and stops) a loop which iterates at the speed set by the Slider Bar. Each iteration generates a new random color map and updates the image. Clicking the Colorize button a second time stops the loop.


