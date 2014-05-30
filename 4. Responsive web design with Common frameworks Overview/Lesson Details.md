## Lesson Details
### HTML5 Markup
#### Responsive Web Design vs Adaptive Web Design
* Responsive web design [1]
  * Web design that fluidly adjusts and responds to any screen size
  * Requires more code and uses fluid CSS (e.g. grids)
  * More considerations when it comes to the design

* Adaptive Web Design
  * Web design that adjusts and responds to a predetermined set of screen sizes
  * Code will only be focused on the supported screen sizes.
  * Less considerations when it comes to the design

### Cross-browser Compatibility
* Reset Stylesheets
  * Browsers have different default values for element styles so we need to "reset" them. [4]
  * Some available CSS reset:
    * Eric Meyer's CSS Reset
    * html5reset.org
    * html5boilerplate.com
  * CSS reset is also available on existing CSS frameworks like Bootstrap
* Fallbacks for less-able browsers
  * Conditional classes for IE
  * Conditional stylesheets for IE
* Modernizr [5]
  * Feature detection
    * Identify what the browser can and cannot do
    * Adds classes to the <html> tag 
    * Apply CSS modifications based on the features detected
  * Polyfill - a JS code that replicates API for the use of older browsers


### Responsive Web Design
#### Desktop Down
* Design your desktop view first then add more CSS styles for smaller views.
  * Hide elements that are not required to be seen on smaller views
  * Start big then filter

#### Mobile-first Approach [6]
* Design your mobile view first. Just add more CSS styles for larger views.
  * Know what's important and display that first - What do you do when you lose 80% of your screen real estate?
  * Start small then enhance
  * Harness mobile functionalities - innovation
  * Styles are defined as they are needed which keeps the file size down [7]

#### Fluid Columns [2]
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
4. [Eric Meyer's "Reset CSS"](http://meyerweb.com/eric/tools/css/reset/)
5. [Modernizr Documentation](http://modernizr.com/docs/#howitworks)
6. [Mobile-First Responsive Web Design](http://bradfrostweb.com/blog/web/mobile-first-responsive-web-design/)
7. [Creating a Mobile-First Responsive Web Design](http://www.html5rocks.com/en/mobile/responsivedesign/)
