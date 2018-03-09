# R Data-Science Samples and Guidelines
## 04 Exploratory Data Analysis
### 06 Graphics Devices in R
#### Questions, Answers, Exercises:

In R, what general procedure is used to plot to an explicitly-created graphics device?  
1. Explicitly launch a graphics device
2. Call a plotting function to make a plot (Note: if you are using a file device, no plot will appear on the screen)
3. Annotate plot if necessary
4. Explicitly close graphics device with "`dev.off()`" (this is very important!)

What R commands will create PDF or SVG vector-format graphics devices?  
- "`pdf`": useful for line-type graphics, resizes well, usually portable, not efficient if a plot has many objects/points
- "`svg`": XML-based scalable vector graphics; supports animation and interactivity, potentially useful for web-based plots

What R commands will create commonly-used bitmat-format graphics devices?  
- "`png`": bitmapped format, good for line drawings or images with solid colors, uses lossless compression (like the old GIF format), most web browsers can read this format natively, good for plotting many many many points, does not resize well
- "`jpeg`": good for photographs or natural scenes, uses lossy compression, good for plotting many many many points, does not resize well, can be read by almost any computer and any web browser, not great for line drawings
- "`tiff`": Creates bitmap files in the TIFF format; supports lossless compression
- "`bmp`": a native Windows bitmapped format

What R commands will create a screen devices on each of Unix/Linux, macOS, or Windows?  
- On Unix/Linux the screen device is launched with "`x11()`"
- On a Mac the screen device is launched with the "`quartz()`"
- On Windows the screen device is launched with "`windows()`"

What R command will list currently-open graphics devices?  
```r
dev.list()
```

What R command will return the currently-active graphics device?
```r
dev.cur()
```

What R command will change the currently-active graphics device?
```r
# Where <integer> is the ID of an open graphics device...
dev.set(<integer>)
```
