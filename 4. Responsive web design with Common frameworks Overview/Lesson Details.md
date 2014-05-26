## Lesson Details
### Responsive Web Design vs Adaptive Web Design
* Responsive web design [1]
  * Web design that fluidly adjusts and responds to any screen size
  * Requires more code and uses fluid CSS (e.g. grids)
  * More considerations when it comes to the design

* Adaptive Web Design
  * Web design that adjusts and responds to a predetermined set of screen sizes
  * Code will only be focused on the supported screen sizes.
  * Less considerations when it comes to the design

### Flexible or Liquid Layout [2]
* Designs usually have layouts that uses fixed dimensions
  * How should we convert these fixed-size layouts to flexible ones?
    * __target ÷ context = result__
    * target is the fixed size of the target element: header is 900px
    * context is the overall fixed size of the viewport: body/viewport is 1000px
    * result will be the new size (in percentage) of the target element: 90%
  * Same formula can be applied to fonts
    * Usually, font sizes are defined using pixels but it is advisable to use ems when defining font sizes as it is flexible by default
    * By default 1em = 16px  thus, the context that will be used in the formula will be 16px
  * Images should have a max-width: 100% CSS property  to accommodate any parent width [3]
    * Fortunately, browsers already scale the image’s height appropriately
    * IE6 doesn’t support max-width so use width: 100% instead, but there are still issues on this: image will be forced to always have the width of the parent container. If the original image is smaller than the container, this can be a problem.

### References
1. [What is the difference between responsive vs. adaptive web design?](http://www.techrepublic.com/blog/web-designer/what-is-the-difference-between-responsive-vs-adaptive-web-design/)
2. [Create Fluid Layouts in HTML5 and CSS3](http://www.creativebloq.com/css3/create-fluid-layouts-html5-and-css3-3142768)
3. [Fluid Images](http://alistapart.com/article/fluid-images)
