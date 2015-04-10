## Website Performance Optimization portfolio project

### Getting started

In order to run the application succesfully follow, please, the following steps:

1. Git clone repository
1. Run a local server inside de repository. This work uses python simple HTTP server module. 

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8000
  ```
1. Open a browser and visit localhost:8000

### Checking page speed

This work uses Grunt task manager and psi-ngrok to compute pagespeed. You should enter following commands to test a pagspeed results:


  ```bash
  $> npm install
  $> grunt
  ```

### 60fps Optimization 

Visit http://localhost:8000/views/pizza.html with google chrome browser and open developer Tools


## Optimizations

1. PageSpeed

In order to optimize critical-rendering-path index.html has been modified by inlining stylesheets and reordering head resources. Moreover, all images have been compressed to avoid high download timings.

1. Pizza.html and views/js/main.js 

main.js: changePizzaSizes and updatePositions have been modified and lines 456 and 513 reflect the final changes. There was needed to take out this lines from loops. Once calculation was enough.

Finally in order to achieve 60fps the main optimization was to improve performance of fixed position elements by introducing [backface-visibility: hidden;](http://benfrain.com/improving-css-performance-fixed-position-elements/).

## References

1. [Deloper Chrome](https://developer.chrome.com/devtools/docs/network)
1. [Chrome Dev Summit 2013](https://www.youtube.com/watch?v=YyQYhhy1dZI)
1. [Accelerated Rendering in Chrome](http://www.html5rocks.com/en/tutorials/speed/layers/)
1. [Avoiding Unnecessary Paints](http://www.html5rocks.com/en/tutorials/speed/unnecessary-paints/)
1. [CSS Paint Times and Page Render Weight](http://www.html5rocks.com/en/tutorials/speed/css-paint-times/)
1. [Smashing Magazine](http://www.smashingmagazine.com/2013/06/10/pinterest-paint-performance-case-study/)
1. [Improving the CSS performance of fixed position elements](http://benfrain.com/improving-css-performance-fixed-position-elements/)
1. [Schrolling Performance](http://www.html5rocks.com/en/tutorials/speed/scrolling/)
1. [Why Moving Elements With Translate() Is Better Than Pos:abs Top/left](http://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/)