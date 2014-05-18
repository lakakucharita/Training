## HTML5 & CSS3 overview (2 sessions 1.5/each)
### Brief Overview of HTML/CSS Development (10 minutes)
* **What has changed from HTML4 to HTML5** [1]
 * New elements for better structure (ex. article, section, nav)
 * New Feature APIs (ex. media element APIs, offline API)
 * New and updated attributes for existing elements (ex. new types for inputs)
 * Obsoleted elements and attributes (ex. basefont, frameset, applet, "version" in html)
* **What has changed from CSS2/2.1 to CSS3** [2]
 * New properties (ex. box-shadow, border-radius)
 * New functions (ex. calc(), media queries)
 * New selector matches and pseudo-classes (ex. element[attribute*="value"], :nth-child, :nth-last-of-type, )
* **Should you start coding with HTML5/CSS3?**
 * **Yes...** 
   - As more users continue to adopt modern browsers, our websites should be ready to take advantage of these features to give users a better user experience when available
    - Eventually these will become the baseline standards for web development, and old code may obsoleted if not brought up to speed
 * **...but with caution!**
   - A large percentage of our users still use legacy browsers like IE8 and below, which do not support HTML5 and CSS3
    - Our websites' functionality and presentation should not become entirely dependent on HTML5 and CSS3 alone; they should not become crutches to development

### Notable HTML5 Tags (30 minutes)
####**Semantic Elements** [3]
* **header** represents a group  of introductory or navigational aids. A header element is intended to optionally contain the section’s heading (an h1–h6 element or an hgroup element), but this is not required. It isn also used to wrap a section’s table of contents, a search form, or any relevant logos.
```html
   <header>
      <h1>My Site</h1>
      <p>Welcome to my site!</p>
   </header>
```
* **hgroup** represents the heading of a section. It is used to group a set of h1–h6 elements when the heading has multiple levels, such as subheadings, alternative titles, or taglines.
```html
   <hgroup>
      <h1>Connecting customers to opportunities</h1>
      <h2>HSBC aims to be where the growth is, helping businesses to thrive and economies 
          to prosper and enabling people to realise their ambitions. HSBC Group Chief 
          Executive Stuart Gulliver outlines the Group's strategy and purpose.</h2>
   </hgroup>
   <article>...</article>
```
* **footer** represents a footer for its nearest ancestor sectioning content or sectioning root element. Typically contains information about its section such as its author, links to related documents, copyright data, and similar. When contianing entire sections, a footer can represent appendices, indexes, long colophons, verbose license agreements, and other such content. Not required to be placed at the end of a document.
```html
   <footer>
      <nav>
         <p>
            <a href="/terms.html">Terms and conditions</a>
            <a href="/privacy.html">Privacy policy</a>
            <a href="/cookies.html">Cookie policy</a>
            <a href="/accessbility.html">Accessibility policy</a>
         </p>
      </nav>   
      <p>No endorsement or approval of any third parties or their advice, opinions, 
         information, products or services is expressed or implied by any information 
         on this Site or by any hyperlinks to or from any third party websites or pages. 
         Your use of this website is subject to the terms and conditions governing it. 
         Please read these terms and conditions before using the website.</p>
   </footer>
```
* **section** represents a generic document or application. Essentially a thematic grouping of content, typically with a heading. Should be used for content segregation and division for major sections; for example, chapters or numbered sections for online documentation; or for an article page, sections can be used to segregate the introduction, articles, and contact information.
```html
   <article>
      <hgroup>
         <time datetime="2014-05-07">07 May 2014</time>
         <h1>Connecting customers to opportunities</h1>
         <p class="author">by Stuart Gulliver</p>
         <p class="role">HSBC Group Chief Executive</p>
      </hgroup>
      <section>
         <p>HSBC opened for business in Hong Kong and Shanghai in 1865. Since then, 
            the world has witnessed many periods of political and economic turbulence 
            but HSBC has grown and thrived, thanks to its ability to adapt. We constantly 
            reassess how we can best serve our customers in meeting the challenges and 
            opportunities of the times in which we live.</p>
      </section>
      <footer>
         <p>Related content</p>
         <section>
            <hgroup>
               <h1>HSBC Holdings plc Interim Management Statement 1Q 2014</h1>
               <time datetime-"2014-05-07">07 May 2014</time>
               <p>Reported profit before tax (‘PBT’) down 20% in 1Q of 2014…</p>
            </hgroup>
         </section>
         <section>
            <hgroup>
               <h1>HSBC Holdings plc Annual Results 2013</h1>
               <time datetime-"2014-02-24">24 Feb 2014</time>
               <p>Reported profit before tax (‘PBT’) up 9% in 2013 at US$22,565m…</p>
            </hgroup>
         </section>
      </footer>
   <article>
```
* **nav** represents a section of a page that links to other pages or to parts within the page: a section with navigation links. Not all groups of links on a page need to be in a nav element — only sections that consist of major navigation blocks are appropriate for the nav element. Not required for footer links to common pages, such as "Terms and Conditions", etc.
```html
   <section>
      <hgroup>
         <h1>About HSBC</h1>
         <h2>in About HSBC</h2>
         <p>Learn about our history, our purpose, and our strategy to become 
            the world's leading international bank. Get information on our leadership 
            team and our global network.</p>
      </hgroup>
      <nav>
         <ul>
            <li><a href="/purpose.html">Our purpose</a></li>
            <li><a href="/strategy.html">Our strategy</a></li>
            <li><a href="/leadership.html">Leadership</a></li>
            <li>...</li>
         </ul>
      </nav>
   </section>
   <section>...</section>
```
* **article** represents a component of a page that consists of a self-contained composition in a document, page, application, or site and that is intended to be independently distributable or reusable, e.g. in syndication. Essentially an independent item of content.
```html
   <article>
      <hgroup>
         <time datetime="2014-05-07">07 May 2014</time>
         <h1>Connecting customers to opportunities</h1>
         <p class="author">by Stuart Gulliver</p>
         <p class="role">HSBC Group Chief Executive</p>
      </hgroup>
      <section>
         <p>HSBC opened for business in Hong Kong and Shanghai in 1865. Since then, 
            the world has witnessed many periods of political and economic turbulence 
            but HSBC has grown and thrived, thanks to its ability to adapt. We constantly 
            reassess how we can best serve our customers in meeting the challenges and 
            opportunities of the times in which we live.</p>
         <p>...</p>
      </section>
      <footer>...</footer>
   <article>
   <article>...</article>
```
* **aside** represents a section of a page that consists of content that is tangentially related to the content around the aside element, and which could be considered separate from that content. Can be used for typographical effects like pull quotes or sidebars and for other content considered separate from the main content of the page.
```html
   <article>
      <hgroup>
         <time datetime="2014-05-07">07 May 2014</time>
         <h1>Connecting customers to opportunities</h1>
         <p class="author">by Stuart Gulliver</p>
         <p class="role">HSBC Group Chief Executive</p>
      </hgroup>
      <section>
         <p>HSBC opened for business in Hong Kong and Shanghai in 1865. Since then, 
            the world has witnessed many periods of political and economic turbulence 
            but HSBC has grown and thrived, thanks to its ability to adapt. We constantly 
            reassess how we can best serve our customers in meeting the challenges and 
            opportunities of the times in which we live.</p>
         <p>Today, a great shift in the world economy is well underway. Economic power is 
            moving east and south; by the middle of this century the collective size of 
            the economies we currently deem “emerging” will have increased five-fold and 
            become larger than the developed world.</p>
         <aside>
            <q>We are committed to growing the business and dividends, implementing the 
               highest global standards of conduct and compliance.</q>
         </aside>
         <p>...</p>
      </section>
      <footer>...</footer>
   <article>
```
* **time** represents either a time on a 24 hour clock, or a precise date in the proleptic Gregorian calendar, optionally with a time and a time-zone offset, that is machine-readable.
```html
   <article>
      <hgroup>
         <time datetime="2014-05-07T06:30+00:00">07 May 2014</time>
         <h1>Connecting customers to opportunities</h1>
         <p class="author">by Stuart Gulliver</p>
         <p class="role">HSBC Group Chief Executive</p>
      </hgroup>
      <section>...</section>
      <footer>...</footer>
   <article>
```
* **mark** represents a run of text in one document marked or highlighted for reference purposes.
```html
   <article>
      <hgroup>...</hgroup>
      <section>
         <p>HSBC opened for business in Hong Kong and Shanghai in 1865. Since then, 
            the world has witnessed many periods of political and economic turbulence 
            <mark>but HSBC has grown and thrived, thanks to its ability to adapt</mark>. 
            We constantly reassess how we can best serve our customers in meeting the 
            challenges and opportunities of the times in which we live.</p>
         <aside>
            <q>We are committed to growing the business and dividends, implementing the 
               <mark>highest global standards of conduct and compliance</mark>.</q>
         </aside>
         <p>...</p>
      </section>
      <footer>...</footer>
   <article>
```

####**Input Types** [4]
<sub>_Note: Performance for these inputs are currently not consistent across all HTML5-capable browsers, and should be used with caution. But a lot of these have the potential to replace JavaScript widget soffering similar functionality, garnering them some special notice._</sub>

For a sample demo, please see [Course 3 HTML5 CSS3 Sample Code.html](3. HTML5 & CSS3 overview/Course 3 HTML5 CSS3 Sample Code.html)

* **date, datetime, and datetime-local** specifies an input for entering a date, a UTC-formatted date and time, or a local date and time, respectively. The **date** and **datetime-local** inputs have a built-in calendar date picker for easy data entry (returning values in _MM/DD.YYYY_ and _MM/DD/YYYY, HH:MM AM/PM_ values, respectively), while the **datetime** input accepts a string.
```html
<input type="date">
<input type="datetime">
<input type="datetime-local">
```
* **month, time, and week** similar to the date input type, the **month** and **week** inputs have a built-in calendar date picker for easy data entry (returning values in _Month YYYY_ and _Week ##, YYYY_ values, respectively), while the **time** input accepts a pre-formatted string returning a value in _HH:MM AM/PM_ format.
```html
<input type="month">
<input type="time">
<input type="week">
```
* **color** specifies an input for selecting a color from a built-in color picker. The value returned is the chosen color's hex code. A preset color value can be set using the "value" attribute.
```html
<input type="color" value="#db0000">
```
* **email** specifies an input that only accepts a valid string in email address format, and returns the string value. It is automatically validated on form submission.
```html
<input type="email">
```
* **tel** specifies an input that accepts a string, and returns the value. A regular expression can also be set with the "pattern" attribute for validation.
```html
<input type="tel" pattern="[0-9]{10}">
```
* **search** connects to a dataset. The **search** input then takes in a string and searches the dataset for a match; if successful, it returns the matching value. Also provides built-in suggestions and autocomplete functions.
```html
<input type="search" list="search-engines">
<datalist id="search-engines">
   <option value="Google">
   <option value="Yahoo">
   <option value="Bing">
   <option value="Duck Duck Go">
</datalist>
```
* **range** is an input type that generates a slider and returns number-related values. Minimium and maximum ranges are set using the "min" and "max" attributes, respectively.
```html
<input type="range" min="1" max="10">
```
* **number** accepts only numbers for input and returns the value. Validation is automatically done on form submission. A quantifying range can also be optionally set using the "min" and "max" attributes.
```html
<input type="number" min="1" max="5">
```
* **url** accepts a string in the format of a URL address. Validation is automatically done on form submission and returns the value.
```html
<input type="url">
```

### HTML5 Feature APIs (20 minutes) [3]
* **Canvas** in a nutshell is a rectangle in your page where you can use JavaScript to draw anything you want in real-time. You can have more than one <canvas> element on the same page. Each canvas will show up in the DOM, and each canvas maintains its own state. If you give each canvas an id attribute, you can access them just like any other element.
```html
<canvas id="myCanvas" width="300" height="225"></canvas>
```
* **Video and Audio** elements allow direct embedding of media content into HTML pages. However, these can be tricky to use as there are no defined universal HTML5 video and audio codecs for playback across all browsers; as a result, multiple file types (specifically OGG/MP4/WEBM for video, and OGG/MP3/WAV for audio) need to be embedded for cross-browser performance and to support mobile devices. The **video** element can accept subtitle tracks in VTT format.
```html
<video width="320" height="240" controls>
   <source src="movie.mp4" type="video/mp4">
   <source src="movie.ogg" type="video/ogg">
   <source src="movie.webm" type="video/webm">
   <track src="subtitles_en.vtt" kind="subtitles" srclang="en" label="English">
</video>
<audio controls>
   <source src="audio.ogg" type="audio/ogg">
   <source src="audio.mp3" type="audio/mpeg">
   <source src="audio.mp3" type="audio/wav">
</audio>
```
* **Local Storage** is a feature in HTML5 for websites to store information on your computer and retrieve it later. Unlike cookies, it is built for large quantities of information and does not require any additional HTTP requests once instantiated, accessed instead via JavaScript. Local Storage makes use of key/value pairs to store information. Currently limited to string-to-=string mappings. Another limitation: saved information is stored on local computer only.

* **Web Workers** provide a standard method for browsers to run JavaScript in the background, spawning multiple “threads” that all run at approximately the same time. These “background threads” can do complex mathematical calculations, make network requests, or access local storage while the main web page responds to the user scrolling, clicking, or typing. Useful for web applications that make use of real-time data rendering and computations.
* **Geolocation** feature allows users to provide their location to web applications; simply put, it exposes latitudinal and longitudinal information to JavaScript on a page. Can be difficult to use depending on the positioning hardware of the user; mobile devices will provide geolocation data easily, while desktop computers may not have the necessary networking equipment to connect to the API. Also, the API requires opting-in with explicit permission from the user.
* **Offline Support** enables websites to function offline without an internet connection. When enabled on a website, the web server instructs the browser to download specific assets needed to function offline. These instructions are in the form of a cache manifest file. Mostly used in mobile websites when saved to a home screen of a mobile device.
* **History** API in HTML5 provides a standardized way to manipulate the browser history via script. You can add entries to the browser history, and respond when those entries are removed from the stack by the user pressing the browser’s back button. This means that the URL can continue to do its job as a unique identifier for the current resource, even in script-heavy applications that don’t ever perform a full page refresh. Great for MVC applications.


### CSS3 Features and Properties (30 minutes) [5]
* **CSS length calculations** is possible in CSS3 using the calc() property, which lets you do basic math calculations to compute a length value. Useful for computing widths and heights and compensating for margins.
```html
   <div class="wrapper">
      <div class="side">...</div>
      <div class="main">...</div>
   </div>
```
```stylesheet
   .wrapper{
      width:80%;
      position:relative;
   }
   .side{
      width:80px;
      position:relative;
      margin-right:1em;
      background:#F60;
   }
   .main{
      width:calc(100% - 1em);
      position:relative;
      background:#FC0;
   }
   
```
* **Border-radius, border-image, and outline** are additional border decorations for elements. *Border-radius* lets you create rounded corners, while *border-image* allows you to specify an image file to fill the border, provided you set a border width first. *Outline* is similar to border (including the shorthand), except it is not included in the outlined element's computed width and height, instead the outline is drawn above the element.
```html
   <div class="rounded-div">...</div>
   <div class="circle-div">...</div>
   <div class="bordered-div">...</div>
   <div class="outlined-div">...</div>
   <p class=outlined-text>Hello world</p>
```
```stylesheet
   .rounded-div{
      height:100px;
      width:200px;
      border-radius:20px 10px 40px 80px
   }
   .rounded-div{
      height:100px;
      width:100px;
      border-radius:50%;
   }
   .bordered-div{
      height:20px;
      width:100px;
      border-width: 10px 20px 5px 25px;
      border-image: url("border-image.png") 10 20 5 25 repeat stretch;
   }
   .outlined-div{
      height:100px;
      width:100px;
      outline:4px solid #DB0000;
   }
   .outlined-text{
      height:100px;
      width:100px;
      outline:4px solid #DB0000;
   }
```

* **Box-shadow and text-shadow** lets you add native shadows to block and text elements, respectively. With **box-shadow** you can specify whether it is inset or not, the offset length, apply multiple shadows, and also the blur radius, spread and color. For **text-shadow** you can set the offset length and blur radius.
```html
<div class=“boxshadow”>
<p class=“textshadow”>The quick brown fox jumped over the lazy dog.</p>
</div>
```
```stylesheet
.boxshadow{
background:#999;
box-shadow:8px 8px 12px 8px #000;
}
.textshadow{
margin:12px;
color:#FFF
text-shadow:8px 4px 2px #DB0000;
}
```
* **Gradients and RGBA, opacity** allows setting background color gradients. Combined with RGBA, it is also possible to customize your own gradient steps and with differing levels of opcacity. Opacity can also be set as a separate CSS property. One issue with gradients is its lack of unified support across browsers, requiring multiple vendor-prefixed gradient properties to ensure consistent rendering. IE6-9 in particular use a different property for gradients, **filter**, which does not support all gradient directions.
```html
<div class="outerbox">
   <div class="innerbox">...</div>
</div>
```
```stylesheet
.outerbox{
   height:100px;
   width:100px;
   position:relative;
   overflow:visible;
   background: linear-gradient(135deg, rgba(30,87,153,1) 0%,rgba(41,137,216,0) 50%,rgba(32,124,202,0.02) 51%,rgba(125,185,232,1) 100%);
}
.innerbox{
   height:80px;
   width:200px;
   position:aboslute;
   top:30px;
   left:30px;
   background: linear-gradient(to bottom, #ff3019 0%,#9e0303 100%);
   opacity:0.8;
}
```
* **Counters** are native CSS variables which values may be incremented using CSS rules to keep track of how many times an element is used. The value of a counter is manipulated through the use of _counter-reset_ and _counter-increment_ properties, which can be displayed on a page using the _counter()_ or _counters()_ function of the _content_ property.
```html
<ol class="level1">
   <li>This is Item 1</li>
   <li>This is Item 2</li>
   <ol class="level2">
      <li>This is Item 2.1</li>
      <li>This is Item 2.2</li>
      <ol class="level3">
         <li>This is Item 2.1.1</li>
      </ol>
   </ol>
</ol>
```
```stylesheet
ol{
   counter-reset:level;
   list-style-type: none;
}
li:before {
  counter-increment: level;
  content: counters(level,".") " > "; 
}
```
* **Web and Icon Fonts** lets developers specify their own custom fonts for use in their websites. Icon fonts are also possible using SVG-generated webfonts.
```html
<p class="myfont">This line of text uses a custom webfont called Roboto. Below you'll find a couple of icons from a custom icon font.</p>
<p class="myicons">&#x25b2; &#x25b6; &#x25bc; &#x25b4; &#x2795; &#x2796; &#x2715;</p>
<p class="myicons">&#xe60a;</p>
```
```stylesheet
@font-face {
    font-family:"Roboto";
    src:url("webfonts/roboto.medium.eot");
    src:url("webfonts/roboto.medium.eot?#iefix") format("embedded-opentype"),
        url("webfonts/roboto.medium.ttf") format("truetype"),
        url("webfonts/roboto.medium.woff") format("woff"),
	url("webfonts/roboto.medium.svg#robotomedium") format("svg");
    font-weight:normal;
    font-style:normal;
}
.myfont{
    font-size:1.2em;
    font-family:"Roboto", sans-serif;
}
@font-face {
    font-family:"Icons";
    src:url("../webfonts/erik.escueta.net.icons.eot");
    src:url("../webfonts/erik.escueta.net.icons.eot?#iefix") format("embedded-opentype"),
	url("../webfonts/erik.escueta.net.icons.ttf") format("truetype"),
	url("../webfonts/erik.escueta.net.icons.woff") format("woff"),
	url("../webfonts/erik.escueta.net.icons.svg#icons") format("svg");
    font-weight: normal;
    font-style: normal;
}
.myicons{
    font-size:1.2em;
    font-family:'Icons' !important;
    speak:none;
    font-style:normal;
    font-weight:normal;
    font-variant:normal;
    text-transform:none;
    line-height:1;
    -webkit-font-smoothing:antialiased;
    -moz-osx-font-smoothing:grayscale;
}
```
* **Media Queries** gives you the ability to specify diffent CSS classes and properties for different media types and viewport properties.
```html
<div class="mobile">...</div>
<div class="desktop>...</div>
```
```stylesheet
@media screen and (max-width:640px){
    .mobile{display:inherit;}
    .desktop{display:none;}
}
@media screen and (min-width:641px){
    .mobile{display:none;}
    .desktop{display:inherit;}
}
```
* **Multiple Backgrounds** allows assigning more than one image to the **background-image** property using a comma-separated value syntax, with the first declared image as the topmost layer then wprking downwards through the stack. To apply different **background** properties to each image, the same comma-separated value syntax is used in correlation. For easier input, a shorthand syntax can also be used.
```html
   <div class="mybackgrounds">...</div>
```
```stylesheet
   .mybackgrounds{
      background:url("background1.jpg") center center no-repeat #000, url("background2.jpg") top left no-repeat, url("background3.jpg") bottom right no-repeat, url("background4.jpg") repeat cover;
   }
```
* **CSS Columns** automatically convert an element block into columns, with native properties for setting the column gaps and rules for size and style.
```html
   <p class="three-columns">HSBC is one of the world's largest banking and financial services organisations. With more than 6,300 offices in both established and emerging markets, we aim to be where the growth is, connecting customers to opportunities, enabling businesses to thrive and economies to prosper, and, ultimately, helping people to fulfil their hopes and realise their ambitions. We serve around 54 million customers through our four Global Businesses: Retail Banking and Wealth Management, Commercial Banking, Global Banking and Markets, and Global Private Banking. Our network covers 75 countries and territories in Europe, the Asia-Pacific region, the Middle East, Africa, North America and Latin America. Listed on the London, Hong Kong, New York, Paris and Bermuda stock exchanges, shares in HSBC Holdings plc are held by about 216,000 in 131 countries and territories.</p>
```
```stylesheet
.three-columns{   
   column-count:3;
   column-gap:40px;
   column-rule:3px outset #ff00ff;
}
```

### CSS3 Properties under consideration (15 minutes) [2]
* **Animations, Transitions and Transforms** i simplest form use CSS to animate elements, similar to the animation functions used in frameworks like jQuery. In general CSS animations are mainly divided into two components: **transitions** for animation properties, and **transforms** for visual manipulation. Another side component, **translate**, is essentially a grouping of multiple transforms. While CSS animations are faster than JavaScript animations and use less memory calculations, they also primarily use hardware acceleration which can be detrimental for mobile devices.
```html
<div class="myanimation">...</div>
```
```stylesheet
.myanimation{
   transition: all 0.5s ease;
   background-color:#000;
}
.myanimation:hover{
   transform:translate(20px, 10px) rotate(90deg) skewX(25deg);
   background-color:#DB0000;
}
```
* **CSS Animation Keyframes** allow greater granularity in defining CSS animations, by adding an **@keyframes** rule that contains your specific animation steps. You use percentages to define your animation step positions in the total playback time, or simply From-To (which is from 0% to 100% in the timeline).
```html
<div class="myanimation">...</div>
```
```stylesheet
.myanimation{
   background-color:#000;
}
.myanimation:hover{
   animation:mykeyframes  0.5s ease infinite;
}
@keyframes mykeyframes {
   0%{height:0px;}
   50%{height:300px; transform:translate(20px, 10px) rotate(90deg) skewX(25deg); background-color:#DB0000;}
   100%{height:0px;}
}
```
* **CSS Animation Callbacks** specifies a JavaScript function to be called when a CSS animation is finished running. The callback is globally set via JavaScript, and requires further setup if you want to execute callbacks only for specific CSS animations. Not as simple to set up as in other JavaScript frameworks like jQuery, where you can run a callback on a specific event bubble.

* **Box-sizing and Flexbox** are new methods for adjusting the box model computations for HTML elements. **Box-sizing** when given the "border-box" value makes padding inclusive of width calculations, as opposed to the default "content-box" where padding isn't part of the visible width (declared or inherited). The ```box-sizing:border-box``` property setting is technically the same as elements in Quirks Mode of IE6 ad below. **Flexbox** is a layout mode, set using the property ```display:flex``` or ```display:inline-flex```. **Flexbox** is essentially a native CSS layout mode for creating a flexible grid layout without the need for floats. Also, the margins of a Flexbox container do not collapse with the margins of its contents for easier UI debugging and refinement.
![An example of Flexbox from MDN](https://developer.mozilla.org/files/3739/flex_terms.png)

### Browser Compatibility and Progressive Enhancement (15 minutes)
* **Cross-Browser and Multi-version Support** [6]

Currently, many CSS3 selectors, features and properties are enabled and available on the latest versions of Chrome, Safari and Firefox in both desktop and mobile. The same holds true as well for HTML5 features, tags, and APIs. However, with regards to Internet Explorer, shims or JavaScript libraries are needed to get them working in IE8, and very few in a limited capacity on IE7 and below. IE9 also has some limited HTML5 and CSS3 support, with performance and covergae only on par with other browsers starting in IE10.

It also beggars consideration that a number of CSS3 properties have proprietary implementations in specific browsers, requiring vendor prefixing befire they can be rendered. Webkit, for example, would require a ```-webkit``` prefix; while Firefox requires ```-moz``` in specific CSS3 properties to render in Firefox.

* **Progressive Enhancement vs. Graceful Degradation - Which is better?** [7]

Given the lack of consistency across browser platforms, there is considerable risk to using HTML5 and CSS3 in production, especially when supporting legacy browsers like IE8 and below. There are two approaches available to address this concenrn.

**Graceful degradation** focuses on building websites for the most advanced and capable browsers first, then patching them to work in older browsers. An example: building an article page layout using HTML5 tags or CSS3 properties, then patch any inconsistencies for unsupported browsers. Naturally, this means your wbesite's experience will not be consistent across all browsers, and may entail a lot of workarounds to get it working on older browsers.

**Progressive enhancements** in contrast takes a content-focused approach. Using the previous example, the article page layout is first built by structuring the content without using HTML5 or CSS3. Once the structure is deemed consistent in your target browsers - uncluding older ones - then you can start adding HTML5 or CSS3 features and properties to enhance your site for users with modern browsers.

With this in mind, it is recommended to approach your UI development with **Prrogressive Enhancement** to keep everything balanced between browsers and your code clean without patchworks or workarounds. Just because we **can** use it doesn't mean we **need** to use it; making a page work and display consistently everywhere is more important than adding new features and tags.

* **Progressive Enhancement Techniques** [8]
  - **Separation of Concerns**
  
In order to execute progressive enhancement in your pages, you must be able to separate your HTML and CSS code into meaningful and logical modules or blocks according to the very structure of your content. For example, while having everything in a single stylesheet may reduce your HTTP calls, it does not help the user to load everything all at once when not all of the code contained is needed - it may even lengthen the initial page load. Likewise, when coding your HTML markup, you should ensure that tags and classes do not overlap, nor should they collapse; otherwise, maintenance becomes an impossible chore. Furthermore, combining CSS classes on elements may cause unintended consequences such as collapsible margins and cross-browser inconsistencies.

It behooves us as web developers to learn how to structure our HTML and CSS code to lessen the confusion between our fellow developers and to ensure an optimal experience for our users.
  - **Multiple Stylesheets and Stylesheet Targeting**

Separating your stylesheets is one approach for progressive enhancement. By segregating your stylesheets, you can cherry-pick which ones are needed for the initial load, and then just load in others as required by the user's actions. In that regard, you can also use multiple stylesheets using ```@import``` in your CSS to load in HTML5 or CSS3 features if a user is, say, in a modern browsing environment; otherwise, the baseline stylesheets will serve adequately. You can also load a separate stylesheet for printing if a user requests it, using the ```media``` query property.
```stylesheet
@import 'screen.css' screen;
@import 'print.css' print;
@import url("chrome://communicator/skin/");
@import "common.css" screen, projection;
@import url('landscape.css') screen and (orientation:landscape);
```
That said, caution must also be exercised that you do not split your stylesheets too thin. A good foundation or focal point for defining your baseline would be by defining your content, and separate your classes accordingly to the content structure and requirements.
  - **Conditional Classes and Comments**
Another method for progressive enhancement - which can also be used in conjunction with the previous approach - is to granularize and define classes and stylesheets for specific browsers natively using conditional comments. One popular method is to catch whether the user's browser is Internet Explorer using IE conditional comments:
```html
<body>
	!--[if lte IE 6]>
   	<div class="ie-browser old-ie"
	<![endif]-->
	<!--[if IE 7]>
   	<div class="ie-browser ie7"
	<![endif]-->
	<!--[if IE 8]>
	<div class="ie-browser ie8"
	<![endif]-->
	<!--[if gte IE 9]>
	<div class="ie-browser modern-ie"
	<![endif]-->
	<!--[if !IE]> -->
	<div class="modern-browser">
	<!-- <![endif]-->
	
		...[some content]...

	</div>
</body>
```
```stylesheet
	.ie-browser{/*styles for IE*/}
	.ie-browser.ie8{/*styles for IE8*/}
	.modern-browser{/*Styles for browsers not IE*/}
```

Combining these methods efficiently will help you achieve proper progressive enhancement in your pages, which in turn will help your users.

### References
1. **HTML5 Differences from HTML4** (http://html-differences.whatwg.org)
2. **CSS3 Overview - Mozilla Developer Network** (https://developer.mozilla.org/en-US/docs/Web/CSS/CSS3)
3. **Dive Into HTML5** (http://diveintohtml5.info)
4. **A Guide to HTML5 Input Types** (http://sixrevisions.com/html5/new-html5-form-input-types/)
5. **12 Awesome CSS3 Features** (http://tutorialzine.com/2013/10/12-awesome-css3-features-you-can-finally-use/)
6. **Can I Use? Browser Compatability Tables for Modern Web Features** (http://caniuse.com)
7. **A List Apart: Understanding Progressive Enhancement** (http://alistapart.com/article/understandingprogressiveenhancement)
8. **A List Apart: Progressive Enhancement with CSS** (http://alistapart.com/article/progressiveenhancementwithcss)
9. **CSS Tricks** (http://css-tricks.com/)
