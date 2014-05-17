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
    - Our websites' functionality and presentation should not become entirely dependent on HTML5 and CSS3 alone; they should not become crutches

### Notable HTML5 Tags (25 minutes)
* **Semantic Elements** [3]
 * **header**
Represents a group  of introductory or navigational aids. A header element is intended to optionally contain the section’s heading (an h1–h6 element or an hgroup element), but this is not required. It isn also used to wrap a section’s table of contents, a search form, or any relevant logos.
```html
   <header>
      <h1>My Site</h1>
      <p>Welcome to my site!</p>
   </header>
```
 * **hgroup**
Represents the heading of a section. It is used to group a set of h1–h6 elements when the heading has multiple levels, such as subheadings, alternative titles, or taglines.
```html
   <hgroup>
      <h1>Connecting customers to opportunities</h1>
      <h2>HSBC aims to be where the growth is, helping businesses to thrive and economies 
          to prosper and enabling people to realise their ambitions. HSBC Group Chief 
          Executive Stuart Gulliver outlines the Group's strategy and purpose.</h2>
   </hgroup>
   <article>...</article>
```
 * **footer**
Represents a footer for its nearest ancestor sectioning content or sectioning root element. Typically contains information about its section such as its author, links to related documents, copyright data, and similar. When contianing entire sections, a footer can represent appendices, indexes, long colophons, verbose license agreements, and other such content.
```html
   <footer>
      <nav>
         <p>
            <a href="/toc.html">Terms and conditions</a>
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
 * **section**
 * **nav**
 * **article**
 * **aside**
 * **time**
 * **mark**

* **Input Types** [4]
 * **date, datetime, and datetime-local**
 * **month, time, and week**
 * **color**
 * **time**
 * **email**
 * **search**
 * **range**
 * **number**
 * **url**

### HTML5 Feature APIs (25 minutes) [3]
* **Canvas**
* **Video and Audio**
* **Local Storage**
* **Web Workers**
* **Geolocation**
* **Offline Support**
* **History**

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
