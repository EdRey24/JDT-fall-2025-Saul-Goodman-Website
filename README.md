# Building Personal/Resume Website: HTML & CSS Workshop

## Overview

This comprehensive guide will walk you through building a complete personal/resume website using HTML and CSS. We'll build this from scratch, explaining each concept in detail as we go, and theme it around Saul Goodman from Breaking Bad/Better Call Saul.

## Workshop Structure

This material is divided into two 1-hour workshops:

### Workshop 1: HTML Fundamentals and Basic Structure
- HTML basics and document structure
- Creating semantic sections
- Building navigation and hero section
- Adding content with proper HTML tags

### Workshop 2: CSS Styling and Responsive Design
- CSS fundamentals and selectors
- Layout techniques (Flexbox and Grid)
- Styling and visual enhancements
- Making the site responsive

## Prerequisites
- A code editor (VS Code)
- A web browser (Chrome, Firefox, Safari, or Edge)

---

# Workshop 1: HTML Fundamentals and Basic Structure

## Understanding the Basics

### What is HTML?
HTML (HyperText Markup Language) is the standard language for creating web pages. It provides the structure and content of a webpage. Think of HTML as the skeleton of a website - it defines the structure but doesn't make it look pretty.

## File Structure
We'll create two files in the same folder:
1. `index.html` - Contains the content and structure
2. `styles.css` - Contains the styling rules

## Step 1: Setting Up the Basic HTML Structure

The DOCTYPE declaration defines the document type and version of HTML. This tells browsers to render the page in standards mode.

The `<html>` tag is the root element of our page. The lang attribute specifies the language of the document's content.

The `<head>` section contains meta information about the document, such as its character encoding, viewport settings, title, and linked resources. This content is not visible to users on the page itself.

The charset `<meta>` tag specifies the character encoding for the document. UTF-8 includes most characters from all human languages.

The viewport `<meta>` tag controls how the page is displayed on devices. width=device-width sets the page width to match the device's screen width. initial-scale=1.0 sets the initial zoom level to 100%.

The `<title>` tag sets the text that appears in the browser tab. This is also used as the page title when bookmarking the site.

The `<link>` tag connects our CSS file to the HTML document. The rel attribute specifies the relationship (stylesheet), and the href attribute specifies the path to the CSS file.

The `<body>` tag contains all the visible content of our webpage. Everything that users see in their browser window goes here.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saul Goodman | Attorney at Law</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
</body>
</html>
```

## Step 2: Creating the Header and Navigation

The `<header>` element represents introductory content or a set of navigational links. It typically contains a logo, navigation, and sometimes a search form.

The `<div>` tag is a generic container for flow content. We're using it with a class="container" to create a centered content area.

The `<nav>` element represents a section of a page that contains navigation links. Screen readers use this to identify the main navigation of the page.

The `<a>` tag defines a hyperlink. The href attribute specifies the link destination. The `<span>` tag is an inline container used to mark up part of a text.

The `<ul>` tag defines an unordered (bulleted) list. The `<li>` tag defines a list item. We're using #section-name to link to different sections of the same page. This is called a fragment identifier or anchor link.

```html
<header>
    <div class="container">
        <nav>
            <a href="#" class="logo">Saul Goodman <span>| Attorney at Law</span></a>
            <ul class="nav-links">
                <li><a href="#ad-video">Commercial</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#skills">Services</a></li>
                <li><a href="#projects">Cases</a></li>
                <li><a href="#testimonials">Testimonials</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </div>
</header>
```

## Step 3: Creating the Hero Section

The `<section>` tag defines a section in a document. The id attribute provides a unique identifier for the section.

The `<img>` tag embeds an image in the document. The src attribute specifies the path to the image. The alt attribute provides alternative text for screen readers and when images can't be displayed.

The `<h1>` to `<h6>` tags represent six levels of section headings. `<h1>` is the highest (most important) level and `<h6>` is the lowest.

The `<p>` tag defines a paragraph.

```html
<section id="hero">
    <div class="container">
        <div class="hero-content">
            <div class="profile-img-container">
                <img src="profile-icon.png" alt="Saul Goodman" class="profile-img">
            </div>
            <h1>Hi, I'm Saul Goodman</h1>
            <p>Did you know that you have rights? The Constitution says you do, and so do I.</p>
            <a href="#contact" class="btn">FREE CONSULTATION</a>
        </div>
    </div>
</section>
```

## Step 4: Creating the Commercial Section

The `<iframe>` tag embeds another HTML page within the current page. We're using it to embed a YouTube video.

```html
<section id="ad-video">
    <div class="container">
        <div class="section-title">
            <h2>Better Call Saul!</h2>
            <p>Watch my latest commercial</p>
        </div>
        <div class="video-container">
            <div class="video-wrapper">
                <div class="video-placeholder">
                    <iframe width="560" height="315" src="https://www.youtube.com/embed/wqnHtGgVAUE" 
                            frameborder="0" allowfullscreen></iframe>
                </div>
            </div>
            <div class="video-description">
                <h3>Why you should call Saul:</h3>
                <ul>
                    <li>24/7 availability for emergencies</li>
                    <li>Creative legal solutions</li>
                    <li>Payment plans available</li>
                    <li>Discretion guaranteed</li>
                </ul>
            </div>
        </div>
    </div>
</section>
```

## Step 5: Creating the About Section

```html
<section id="about">
    <div class="container">
        <div class="section-title">
            <h2>About Me</h2>
        </div>
        <div class="about-content">
            <div class="about-text">
                <h3>Better Call Saul!</h3>
                <p>James Morgan "Jimmy" McGill, better known by my professional alias
                Saul Goodman. I'm a criminal lawyer specializing in helping those
                who find themselves in difficult situations with the law.</p>
                <p>Originally from Cicero, Illinois, I moved to Albuquerque where I
                established my law practice with a simple philosophy: everyone
                deserves a vigorous defense.</p>
                <p>My approach might be unconventional, but I get results. With
                experience ranging from elder law to criminal defense, I've
                successfully represented clients in some of Albuquerque's most
                challenging cases.</p>
                <div class="signature">
                    <p>Saul Goodman, Esq.</p>
                </div>
            </div>
        </div>
    </div>
</section>
```

## Step 6: Creating the Experience Section

For sections like experience where we will be adding more than one professional experience we'll want to copy the div "experience-item" as many times as you want within the "experience-container" div to showcase the various jobs you've had. After copying and pasting as many times as necessary just edit the information within to tailor it to each position.

```html
<section id="experience">
    <div class="container">
        <div class="section-title">
            <h2>Professional Experience</h2>
        </div>
        <div class="experience-container">
            <div class="experience-item">
                <div class="experience-date">2010 - Present</div>
                <div class="experience-content">
                    <h3>Store Manager</h3>
                    <h4>Cinnabon, Albuquerque, NM</h4>
                    <p>Established a successful law practice specializing in criminal
                    defense, personal injury, and elder law.</p>
                </div>
            </div>
        </div>
    </div>
</section>
```

## Step 7: Creating the Services Section

The advice given in the previous step is showcased here where we want to display multiple skills and we do so by coping the div block with the class "skill" and pasting it as many times as needed within out "skills-container" div.

```html
<section id="skills">
    <div class="container">
        <div class="section-title">
            <h2>Legal Services</h2>
        </div>
        <div class="skills-container">
            <div class="skill">
                <h3>Criminal Defense</h3>
                <p>DUI, drug charges, assault, and other criminal matters.</p>
            </div>
            <div class="skill">
                <h3>Civil Litigation</h3>
                <p>From personal injury to contract disputes.</p>
            </div>
            <div class="skill">
                <h3>Elder Law</h3>
                <p>Specializing in cases involving retirement homes.</p>
            </div>
        </div>
    </div>
</section>
```

## Step 8: Creating the Cases Section

This is also similar where you can copy the div class "project" as many times as needed to show every project. In this case since we are theming around Better Call Saul we are using the example of Law Cases but for other professions like programming this can be easily modified by changing the text for softward/hardware projects.

```html
<section id="projects">
    <div class="container">
        <div class="section-title">
            <h2>Notable Cases</h2>
        </div>
        <div class="projects-grid">
            <div class="project">
                <div class="project-img" style="background: linear-gradient(135deg, #8f94fb 0%, #4e54c8 100%);">
                    Sandpiper Crossing
                </div>
                <div class="project-content">
                    <h3>Sandpiper Class Action</h3>
                    <p>Successfully litigated a class-action lawsuit against Sandpiper
                    Crossing retirement community.</p>
                    <a href="#" class="btn">Case Details</a>
                </div>
            </div>
        </div>
    </div>
</section>
```

## Step 9: Creating the Testimonials Section

```html
<section id="testimonials">
    <div class="container">
        <div class="section-title">
            <h2>Client Testimonials</h2>
        </div>
        <div class="testimonials-container">
            <div class="testimonial">
                <div class="testimonial-text">
                    <p>"Saul got me out of a real jam when no other lawyer would take
                    my case. He knows all the angles!"</p>
                </div>
                <div class="testimonial-author">
                    <h4>Badger</h4>
                    <p>Client</p>
                </div>
            </div>
        </div>
    </div>
</section>
```

## Step 10: Creating the Contact Section

The `<form>` tag creates an HTML form for user input. Forms are used to collect user input to send to a server.

The `<label>` tag defines a label for a form element. The for attribute should equal the id attribute of the element it's labeling.

The `<input>` tag specifies an input field where the user can enter data. The type attribute defines what type of input to display. The placeholder attribute specifies a short hint that describes the expected value. The required attribute specifies that an input field must be filled out.

The `<select>` element creates a drop-down list. The `<option>` tag defines an option in a select list.

The `<textarea>` tag defines a multi-line text input control. The rows attribute specifies the visible number of lines in a text area.

The `<button>` tag defines a clickable button. The type attribute specifies the button type (submit, reset, or button).

```html
<section id="contact">
    <div class="container">
        <div class="section-title">
            <h2>Contact Me</h2>
        </div>
        <div class="contact-container">
            <div class="contact-info">
                <h3>Better Call Saul!</h3>
                <p>Don't let legal trouble get you down. I'm here to help 24/7 with
                discreet, effective legal solutions.</p>
                <p>(505) 503-4455</p>
                <p>saul@bettercallsaul.com</p>
                <p>9800 Montgomery Blvd NE, Albuquerque, NM</p>
                <div class="office-hours">
                    <h4>Office Hours:</h4>
                    <p>24/7 - Because legal emergencies don't keep business hours</p>
                </div>
            </div>
            <div class="contact-form">
                <form>
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" class="form-control" placeholder="Your Name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" class="form-control" placeholder="Your Email" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">Phone</label>
                        <input type="tel" id="phone" class="form-control" placeholder="Your Phone">
                    </div>
                    <div class="form-group">
                        <label for="case">Case Type</label>
                        <select id="case" class="form-control" required>
                            <option value="">Select Case Type</option>
                            <option value="criminal">Criminal Defense</option>
                            <option value="civil">Civil Litigation</option>
                            <option value="elder">Elder Law</option>
                            <option value="other">Other</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" class="form-control" placeholder="Describe your situation" rows="5" required></textarea>
                    </div>
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>
        </div>
    </div>
</section>
```

## Step 11: Creating the Footer

The `<footer>` tag defines a footer for a document or section. It typically contains information about the author, copyright, contact, etc.

```html
<footer>
    <div class="container">
        <div class="footer-content">
            <div class="footer-logo">
                <div class="logo">Saul Goodman <span>| Attorney at Law</span></div>
                <p>"When the going gets tough, you don't want a criminal lawyer. You
                want a criminal lawyer."</p>
            </div>
            <div class="footer-links">
                <h4>Quick Links</h4>
                <ul>
                    <li><a href="#about">About</a></li>
                    <li><a href="#experience">Experience</a></li>
                    <li><a href="#skills">Services</a></li>
                    <li><a href="#projects">Cases</a></li>
                    <li><a href="#ad-video">Commercial</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
            <div class="footer-disclaimer">
                <h4>Legal Disclaimer</h4>
                <p>Past results do not guarantee future outcomes. Legal services are
                provided pursuant to the New Mexico Rules of Professional Conduct.</p>
                <p>© 2025 Saul Goodman & Associates. All rights reserved.</p>
            </div>
        </div>
    </div>
</footer>
```

---

# Workshop 2: CSS Styling and Responsive Design

### What is CSS?
CSS (Cascading Style Sheets) is used to style and layout web pages. It controls colors, fonts, spacing, and positioning. If HTML is the skeleton, CSS is the skin and clothing that makes it attractive.

## Step 1: Setting Up Basic CSS Styles

The :root pseudo-class selects the document's root element (html). CSS custom properties (variables) are defined here for consistent theming. Variables are declared with -- prefix and accessed with var() function. This makes it easy to change colors throughout the site by modifying one value.

The * selector targets all elements. We're removing default margins and padding from all elements. box-sizing: border-box includes padding and border in element's total width/height. This makes it easier to size elements consistently.

We're setting a default font stack with fallbacks. line-height: 1.6 improves readability by adding space between lines. We're using our CSS variables for color values. padding-top: 70px creates space for the fixed header.

The .container class creates a centered content area with a maximum width. width: 90% makes it responsive on smaller screens. max-width: 1200px prevents it from getting too wide on large screens. margin: 0 auto centers the container horizontally.

We're adding consistent vertical padding to all sections.

```css
:root {
    --primary: #4e54c8;
    --secondary: #8f94fb;
    --accent: #ff6b6b;
    --light: #f8f9fa;
    --dark: #212529;
    --gray: #6c757d;
    --transition: all 0.3s ease;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: var(--dark);
    background-color: var(--light);
    padding-top: 70px;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 15px;
}

section {
    padding: 80px 0;
}
```

## Step 2: Styling the Header

position: fixed keeps the header at the top when scrolling. top: 0 and left: 0 position it at the top-left corner. width: 100% makes it span the full width of the viewport. box-shadow adds a subtle shadow for depth. z-index: 1000 ensures the header appears above other content.

display: flex creates a flexible box layout. justify-content: space-between distributes items evenly with space between them. align-items: center vertically centers the items.

list-style: none removes the default bullet points from the list.

The :hover pseudo-class applies styles when the user hovers over an element.

```css
header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background: white;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    z-index: 1000;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 0;
}

.logo {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--primary);
}

.logo span {
    font-size: 1rem;
    font-weight: 400;
    color: var(--gray);
}

.nav-links {
    display: flex;
    list-style: none;
}

.nav-links li {
    margin-left: 30px;
}

.nav-links a {
    color: var(--dark);
    font-weight: 500;
}

.nav-links a:hover {
    color: var(--primary);
}
```

## Step 3: Styling the Hero Section

background: linear-gradient() creates a color gradient background. The 135deg parameter sets the angle of the gradient. We're using our CSS variables for the gradient colors. text-align: center centers the text horizontally.

border-radius: 50% makes the image container circular. overflow: hidden ensures the image doesn't overflow the circular container. border adds a semi-transparent white border. rgba() defines a color with red, green, blue, and alpha (transparency) values.

object-fit: cover ensures the image fills the container while maintaining its aspect ratio.

display: inline-block allows setting padding and margin on an inline element. border-radius: 30px creates rounded corners (pill shape). text-transform: uppercase converts text to uppercase. transition: var(--transition) adds smooth transitions for hover effects.

transform: translateY(-3px) moves the button up slightly on hover. box-shadow adds a shadow for a lifted effect.

```css
#hero {
    background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
    color: white;
    text-align: center;
    padding: 120px 0 100px;
}

.hero-content {
    max-width: 800px;
    margin: 0 auto;
}

.profile-img-container {
    width: 200px;
    height: 200px;
    margin: 0 auto 30px;
    border-radius: 50%;
    overflow: hidden;
    border: 5px solid rgba(255, 255, 255, 0.3);
}

.profile-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

#hero h1 {
    font-size: 3.5rem;
    margin-bottom: 20px;
}

#hero p {
    font-size: 1.2rem;
    margin-bottom: 30px;
}

.btn {
    display: inline-block;
    padding: 12px 30px;
    background: var(--primary);
    color: white;
    border-radius: 30px;
    text-transform: uppercase;
    font-weight: 600;
    letter-spacing: 1px;
    transition: var(--transition);
}

.btn:hover {
    background: var(--secondary);
    transform: translateY(-3px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}
```

## Step 4: Styling the Commercial Section

::after is a pseudo-element that creates a virtual element after the selected element. We're using it to create the decorative underline under the section title. position: absolute positions it relative to its nearest positioned ancestor. transform: translateX(-50%) centers it horizontally.

display: flex creates a flexible box layout. flex-wrap: wrap allows items to wrap onto multiple lines if needed. gap: 40px adds space between flex items (replaces margin hacks).

flex: 1 allows the element to grow and shrink as needed. min-width: 300px prevents the element from getting too small.

```css
#ad-video {
    padding: 80px 0;
    background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
}

.section-title {
    text-align: center;
    margin-bottom: 50px;
}

.section-title h2 {
    font-size: 2.5rem;
    color: var(--primary);
    position: relative;
    display: inline-block;
    padding-bottom: 15px;
}

.section-title h2::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 80px;
    height: 3px;
    background: var(--accent);
}

.video-container {
    display: flex;
    flex-wrap: wrap;
    gap: 40px;
    align-items: center;
}

.video-wrapper {
    flex: 1;
    min-width: 300px;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
}

.video-description {
    flex: 1;
    min-width: 300px;
}

.video-description h3 {
    color: var(--primary);
    margin-bottom: 20px;
}

.video-description ul {
    list-style: none;
}

.video-description li {
    margin-bottom: 15px;
}
```

## Step 5: Styling the About Section

text-align: justify creates even text alignment on both sides.

```css
.about-content {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 40px;
}

.about-text {
    flex: 1;
    min-width: 300px;
    text-align: justify;
}

.signature {
    margin-top: 30px;
    padding-top: 20px;
    border-top: 1px solid #eee;
}
```

## Step 6: Styling the Experience Section

The :last-child pseudo-class selects the last element among its siblings.

We're using ::before to create the vertical timeline line.

We're using ::after to create the circular markers on the timeline. box-shadow: 0 0 0 4px rgba(78, 84, 200, 0.2) creates a subtle glow effect.

```css
#experience {
    padding: 80px 0;
    background-color: white;
}

.experience-container {
    max-width: 800px;
    margin: 0 auto;
}

.experience-item {
    display: flex;
    margin-bottom: 40px;
    position: relative;
}

.experience-item:last-child {
    margin-bottom: 0;
}

.experience-item::before {
    content: "";
    position: absolute;
    left: 110px;
    top: 0;
    bottom: 0;
    width: 2px;
    background: var(--secondary);
}

.experience-date {
    width: 100px;
    flex-shrink: 0;
    font-weight: 600;
    color: var(--primary);
    position: relative;
}

.experience-date::after {
    content: "";
    position: absolute;
    right: -16px;
    top: 8px;
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: var(--primary);
    z-index: 1;
    box-shadow: 0 0 0 4px rgba(78, 84, 200, 0.2);
}

.experience-content {
    flex: 1;
    padding-left: 40px;
}

.experience-content h3 {
    color: var(--primary);
    margin-bottom: 5px;
}

.experience-content h4 {
    color: var(--gray);
    font-size: 1.1rem;
    margin-bottom: 10px;
    font-weight: 500;
}
```

## Step 7: Styling the Services Section

```css
#skills {
    background-color: #f8f9fa;
}

.skills-container {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
}

.skill {
    flex: 1;
    min-width: 250px;
    background: white;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
    text-align: center;
    transition: var(--transition);
}

.skill:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
}
```

## Step 8: Styling the Cases Section

display: grid creates a grid layout. grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)) creates a responsive grid. auto-fill automatically places as many items as will fit in the row. minmax(300px, 1fr) sets a minimum column width of 300px and maximum of 1 fraction unit. gap: 30px adds space between grid items.

```css
.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 30px;
}

.project {
    background: white;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
    transition: var(--transition);
}

.project:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
}

.project-img {
    height: 200px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 1.5rem;
    font-weight: 700;
}

.project-content {
    padding: 20px;
}
```

## Step 9: Styling the Testimonials Section

backdrop-filter: blur(10px) creates a frosted glass effect (not supported in all browsers). display: flex with flex-direction: column creates a vertical flex layout. height: 100% ensures all testimonial boxes are the same height.

flex-grow: 1 allows the element to grow to fill available space. This pushes the author information to the bottom of the card.

```css
#testimonials {
    background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
    color: white;
}

#testimonials .section-title h2 {
    color: white;
}

.testimonials-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 30px;
}

.testimonial {
    background: rgba(255, 255, 255, 0.1);
    padding: 30px;
    border-radius: 10px;
    backdrop-filter: blur(10px);
    display: flex;
    flex-direction: column;
    height: 100%;
}

.testimonial-text {
    font-style: italic;
    margin-bottom: 20px;
    flex-grow: 1;
}

.testimonial-author h4 {
    color: white;
    margin-bottom: 5px;
}

.testimonial-author p {
    color: rgba(255, 255, 255, 0.7);
    margin-bottom: 0;
    font-size: 0.9rem;
}
```

## Step 10: Styling the Contact Section

The :focus pseudo-class applies styles when an element has focus (is selected).

resize: vertical allows only vertical resizing of the textarea.

```css
#contact {
    background-color: #f8f9fa;
}

.contact-container {
    display: flex;
    flex-wrap: wrap;
    gap: 40px;
}

.contact-info {
    flex: 1;
    min-width: 300px;
}

.office-hours {
    margin-top: 30px;
    padding-top: 20px;
    border-top: 1px solid #eee;
}

.contact-form {
    flex: 1;
    min-width: 300px;
}

.form-group {
    margin-bottom: 20px;
}

.form-group label {
    display: block;
    margin-bottom: 5px;
    font-weight: 500;
}

.form-control {
    width: 100%;
    padding: 12px 15px;
    border: 1px solid #ddd;
    border-radius: 5px;
    font-size: 1rem;
    transition: var(--transition);
}

.form-control:focus {
    outline: none;
    border-color: var(--primary);
    box-shadow: 0 0 0 3px rgba(78, 84, 200, 0.1);
}

textarea.form-control {
    min-height: 150px;
    resize: vertical;
}
```

## Step 11: Styling the Footer

grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)) creates a responsive grid. auto-fit automatically fits as many columns as possible with the given constraints.

```css
footer {
    background: var(--dark);
    color: white;
    padding: 40px 0;
}

.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 30px;
}

.footer-logo .logo {
    color: white;
}

.footer-links h4,
.footer-disclaimer h4 {
    color: white;
    margin-bottom: 15px;
}

.footer-links ul {
    list-style: none;
}

.footer-links li {
    margin-bottom: 10px;
}

.footer-links a {
    color: rgba(255, 255, 255, 0.7);
}

.footer-links a:hover {
    color: white;
}

.footer-disclaimer p {
    color: rgba(255, 255, 255, 0.7);
    font-size: 0.9rem;
}
```

## Step 12: Making the Site Responsive

Media queries apply different CSS rules based on conditions like screen width. This media query targets screens with a maximum width of 768px (typical mobile devices).

```css
@media (max-width: 768px) {
    body {
        padding-top: 70px;
    }

    .nav-links {
        display: none;
    }

    #hero h1 {
        font-size: 2.5rem;
    }

    .section-title h2 {
        font-size: 2rem;
    }

    .profile-img-container {
        width: 150px;
        height: 150px;
    }

    .video-container {
        flex-direction: column;
    }

    .experience-item {
        flex-direction: column;
    }

    .experience-item::before {
        display: none;
    }

    .experience-date {
        width: 100%;
        margin-bottom: 10px;
    }

    .experience-date::after {
        display: none;
    }

    .experience-content {
        padding-left: 0;
    }

    .nav-links {
        flex-wrap: wrap;
    }

    .nav-links li {
        margin: 5px 15px;
    }
}
```

# Deploy using Github Pages

GitHub Pages is a free service that allows you to host static websites directly from your GitHub repositories.

### Step 1: Configure Publishing Source
1. Navigate to your repository's **Settings** → **Pages**
2. Under **Build and deployment** → **Source**, select **Github Actions**
3. When taken to the **Workflows** tab scroll down to **Pages** and select the Static HTML workflow
4. Leave the workflow as is and just commit changes on the top right
5. Allow the workflow to run and publish your website (This may take a while)
6. Go to your **Deployments** and go to the link Github makes you to see your published website

## Final Thoughts

Congratulations! You've built a complete personal website for Saul Goodman using HTML and CSS. Here are some key concepts we covered:

1. **HTML Structure**: Semantic HTML5 elements for better accessibility and SEO
2. **CSS Layouts**: Flexbox and Grid for creating modern, responsive layouts
3. **CSS Variables**: For consistent theming and easy updates
4. **Responsive Design**: Media queries for adapting to different screen sizes
5. **Pseudo-elements**: For creating decorative elements without extra HTML
6. **Transitions and Transforms**: For adding interactive elements

To continue learning:
1. Add JavaScript to make the navigation work on mobile
2. Implement a working contact form with form validation
3. Add more interactive elements like a image slider for testimonials
4. Learn about CSS preprocessors like SASS
5. Explore CSS frameworks like Bootstrap or Tailwind

Remember, practice is key to mastering HTML and CSS. Try modifying this design or creating your own from scratch!

## Additional Resources

- [MDN Web Docs](https://developer.mozilla.org/) - Comprehensive web technology documentation
- [CSS-Tricks](https://css-tricks.com/) - Tips, tricks, and techniques on using CSS
- [W3Schools](https://www.w3schools.com/) - Web development tutorials
- [FreeCodeCamp](https://www.freecodecamp.org/) - Free coding challenges and projects
- [Odin Project](https://www.theodinproject.com/) - Free courses to learn more in-depth HTML, CSS, and Javascript

Happy coding!
