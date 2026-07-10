My interest in the Mandelbrot set dates back to the August 1985 issue of Scientific American. Around that time, my friend and fellow ex-STSCer, [Bob Smith](https://aplwiki.com/wiki/Bob_Smith), had written a Mandelbrot set explorer in 386 assembly language. It was exceptionally cool.

Fast forward 20ish years to 2006 when I wanted to learn the GUI features of Dyalog APL for Windows. I find it easier to learn when I have a tangible project and so I decided to write a Mandelbrot set explorer in Dyalog APL.

As Dyalog introduced new language features and tools, I'd update the explorer to incorporate them.

* In 2011, Dyalog v13.0 introduced support for complex numbers and 128-bit decimal floating point numbers. While complex numbers might seem a natural fit for the Mandelbrot with each number representing a point in the X-Y plane, they proved to be a bit slow and cumbersome to manipulate. I found it better to maintain 2 vectors representing the X and Y coordinates respectively. However, 128-bit decimal floating point numbers, while a bit slower than 64-bit floats, provided the ability to "zoom" deeper into the set without losing precision.
* In 2014, Dyalog v14.0 released "isolates" which provided some parallel computation capability. By using isolates, I could distribute the computation of the set across multiple APL processes. I described my work in [this blog post](https://www.dyalog.com/blog/2014/08/isolated-mandelbrot-set-explorer/).
  
Over the years, I'd occasionally dust off the explorer and add a new feature like right-click to zoom and various ways to manipulate the color map. I'd also tweak the look and feel to neaten things up a bit.