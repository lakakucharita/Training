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
* **Semantic Elements** [3]
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
* **Input Types** [4]

_Note: Performance for these inputs are currently not consistent across all HTML5-capable browsers, and should be used with caution. But a lot of these have the potential to replace JavaScript widget soffering similar functionality, garnering them some special notice._

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
* **CSS pixel calculations**
* **Border-radius, border-image, and outline**
* **Box-shadow and text-shadow**
* **Gradients and RGBA, opacity**
* **Counters**
* **Web and Icon Fonts**
* **Media Queries**
* **Multiple Backgrounds**
* **CSS Columns**
  
### CSS3 Properties under consideration (15 minutes) [2]
* **Animations, Transitions and Transforms**
* **Box-sizing and Flexbox**
* **Advanced Properties and 3D Transforms**
* **Implementing Callbacks**

### Browser Compatibility and Progressive Enhancement (15 minutes)
* **Cross-Browser and Multi-version Support** [6]
* **Progressive Enhancement vs. Graceful Degradation** [7]
* **Browser detection vs. Feature detection**
* **Progressive Enhancement Techniques using CSS** [8]
 * **Testing for IE**
 * **Conditional Classes**

### References
1. **HTML5 Differences from HTML4** (http://html-differences.whatwg.org)
2. **CSS3 Overview - Mozilla Developer Network** (https://developer.mozilla.org/en-US/docs/Web/CSS/CSS3)
3. **Dive Into HTML5** (http://diveintohtml5.info)
4. **A Guide to HTML5 Input Types** (http://sixrevisions.com/html5/new-html5-form-input-types/)
5. **12 Awesome CSS3 Features** (http://tutorialzine.com/2013/10/12-awesome-css3-features-you-can-finally-use/)
6. **Can I Use? Browser Compatability Tables for Modern Web Features** (http://caniuse.com)
7. **A List Apart: Understanding Progressive Enhancement** (http://alistapart.com/article/understandingprogressiveenhancement)
8. **A List Apart: Progressive Enhancement with CSS** (http://alistapart.com/article/progressiveenhancementwithcss8
