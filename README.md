## HPGLGraphics Library for Processing

This library implements [HPGL](https://en.wikipedia.org/wiki/HPGL) (Hewlett-Packard Graphics Language) file creation from Processing sketches. It works in much the same way as the PDF Export and DXF Export libraries bundled with Processing.

### Getting started 

    import hpglgraphics.*;
    HPGLGraphics hpgl = (HPGLGraphics) createGraphics(width, height, HPGLGraphics.HPGL);
    
    beginRecord(hpgl);
    // do some drawing
    endRecord();

Have a look at the examples included with the library. These demonstrate:

  * line()
  * ellipse()
  * arc() - PIE, CHORD and OPEN
  * rect()
  * vertex()
  * curveVertex()
  * bezierVertex()

### Additional methods

Some additional methods are available for controlling the HPGL output. This include:
  * selectPen(int pen);       // choose another pen (e.g. colour)
  * setPaperSize();           // "A3" or "A4". Landscape orientation is assumed.
  * setPath("filename.hpgl"); // optional. HPGL is output to this file in the sketch directory. The default is "output.hpgl".

### Tips:
  * line() always finishes with Pen Up. To draw continuous joined lines without lifting the pen, use vertex() instead.

To check your HPGL files, I recommend [hp2xx](https://www.gnu.org/software/hp2xx/)

This library was inspired by, and builds upon, these libraries:
  * [HPGL-Plotter](http://sjunnesson.github.io/HPGL-Plotter/)
  * [HPGL](https://github.com/gregersn/HPGL)

The website for the library is [here](https://ciaron.github.io/HPGLGraphics).
Source code is [here](https://github.com/ciaron/HPGLGraphics)
