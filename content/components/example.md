---
title: "Components Example Page"
description: "An example page showing how to use the design components in a real-world scenario"
draft: true
---

# Components Example Page

This page demonstrates how to use the design components in a real-world scenario. It shows how different components can be combined to create a cohesive and visually appealing page.

## Hero Banner - Dark

{{< rawhtml >}}
<div class="component-hero-dark">
  <h1>Welcome to Our Workshop</h1>
  <p>Join us for an intensive coding workshop where you'll learn the latest techniques and best practices for web development.</p>
</div>
{{< /rawhtml >}}

<hr>

```html
<div class="component-hero-dark">
  <h1>Your Heading Here</h1>
  <p>Your descriptive text goes here. This component is perfect for page headers or important announcements that need to stand out.</p>
</div>
```

## Info Box - White

{{< rawhtml >}}
<div class="component-info-white">
  <h3>Workshop Details</h3>
  <p>Our workshop is designed for developers of all skill levels who want to improve their coding skills and learn new technologies.</p>
  <p>The workshop will cover <span class="accent">HTML</span>, <span class="accent">CSS</span>, <span class="accent">JavaScript</span>, and modern frameworks like <span class="accent">React</span> and <span class="accent">Vue</span>.</p>
</div>
{{< /rawhtml >}}

<hr>

```html
<div class="component-info-white">
  <h3>Info Box Title</h3>
  <p>Your information content goes here. You can use <span class="accent">accent</span> spans for highlighting.</p>
</div>
```

## Split Content - Dark

{{< rawhtml >}}
<div class="component-split-dark">
  <div class="content">
    <h3>What You'll Learn</h3>
    <p>During this workshop, you'll gain hands-on experience with the latest web development technologies and techniques. Our experienced instructors will guide you through practical exercises and real-world projects.</p>
  </div>
  <div class="media">
    <pre><code>// Example code
function createComponent() {
  const element = document.createElement('div');
  element.className = 'component';
  return element;
}</code></pre>
  </div>
</div>
{{< /rawhtml >}}

<hr>

```html
<div class="component-split-dark">
  <div class="content">
    <h3>Content Title</h3>
    <p>Your text content goes here. This can be a description, explanation, or any other text-based content.</p>
  </div>
  <div class="media">
    <img src="/path/to/image.jpg" alt="Description">
    <!-- Or you can use code snippets -->
    <pre><code>Your code here</code></pre>
  </div>
</div>
```

## Timeline - White

{{< rawhtml >}}
<div class="component-timeline-white">
  <h3>Workshop Timeline</h3>

  <div class="timeline-item">
    <div class="timeline-date">9:00 AM - 10:30 AM</div>
    <div class="timeline-content">
      <h4>Introduction to Web Development</h4>
      <p>Overview of modern web development practices and technologies.</p>
    </div>
  </div>

  <div class="timeline-item">
    <div class="timeline-date">10:45 AM - 12:15 PM</div>
    <div class="timeline-content">
      <h4>HTML & CSS Fundamentals</h4>
      <p>Deep dive into HTML5 and CSS3 features and best practices.</p>
    </div>
  </div>

  <div class="timeline-item">
    <div class="timeline-date">1:15 PM - 2:45 PM</div>
    <div class="timeline-content">
      <h4>JavaScript Essentials</h4>
      <p>Core JavaScript concepts and modern ES6+ features.</p>
    </div>
  </div>

  <div class="timeline-item">
    <div class="timeline-date">3:00 PM - 4:30 PM</div>
    <div class="timeline-content">
      <h4>Framework Introduction</h4>
      <p>Introduction to popular JavaScript frameworks like React and Vue.</p>
    </div>
  </div>
</div>
{{< /rawhtml >}}

<hr>

```html
<div class="component-timeline-white">
  <h3>Timeline Title</h3>

  <div class="timeline-item">
    <div class="timeline-date">Date or Time</div>
    <div class="timeline-content">
      <h4>Event Title</h4>
      <p>Event description or details.</p>
    </div>
  </div>

  <!-- Additional timeline items -->
</div>
```

## Feature Box - Dark

{{< rawhtml >}}
<div class="three-column">
  <div class="component-feature-dark">
    <h3>Hands-on Learning</h3>
    <p>Practice what you learn with guided exercises and projects that reinforce key concepts.</p>
  </div>

  <div class="component-feature-dark">
    <h3>Expert Instructors</h3>
    <p>Learn from experienced developers who work with these technologies every day.</p>
  </div>

  <div class="component-feature-dark">
    <h3>Small Group Size</h3>
    <p>Limited to 20 participants to ensure personalized attention and support.</p>
  </div>
</div>
{{< /rawhtml >}}

<hr>

```html
<div class="component-feature-dark">
  <h3>Feature Title</h3>
  <p>Description of the feature or service that you want to highlight.</p>
</div>
```

## Card - Dark

{{< rawhtml >}}
<div class="component-card-dark">
  <h3>Sarah Johnson</h3>
  <p>"This workshop completely changed how I approach web development. The instructors were knowledgeable and the hands-on exercises were incredibly valuable."</p>
</div>
{{< /rawhtml >}}

<hr>

```html
<div class="component-card-dark">
  <h3>Card Title</h3>
  <p>Card content goes here. This can include descriptions, features, or any other information.</p>
  <a href="#" class="btn">Call to Action</a>
</div>
```

## Highlight Box - Purple

{{< rawhtml >}}
<div class="component-highlight-purple">
  <h3>Special Offer</h3>
  <p>Register before the end of the month and get a 20% early bird discount! Plus, you'll receive a free e-book on advanced web development techniques.</p>
  <a href="#" class="btn">Register Now</a>
</div>
{{< /rawhtml >}}

<hr>

```html
<div class="component-highlight-purple">
  <h3>Highlight Title</h3>
  <p>Content that needs to be highlighted or emphasized.</p>
  <a href="#" class="btn">Call to Action</a>
</div>
```

## Call to Action - Dark

{{< rawhtml >}}
<div class="component-cta-dark">
  <h2>Join Our Workshop Today</h2>
  <p>Don't miss this opportunity to enhance your web development skills and take your career to the next level.</p>
  <a href="#" class="btn">Sign Up Now</a>
</div>
{{< /rawhtml >}}

<hr>

```html
<div class="component-cta-dark">
  <h2>Call to Action Title</h2>
  <p>Persuasive text encouraging the user to take action.</p>
  <a href="#" class="btn">Action Button</a>
</div>
```

## Additional Resources

Regular markdown content can be mixed with components to create a rich and varied page layout. Here's a list of additional resources:

1. [MDN Web Docs](https://developer.mozilla.org)
2. [CSS Tricks](https://css-tricks.com)
3. [JavaScript.info](https://javascript.info)
4. [React Documentation](https://reactjs.org)
5. [Vue Documentation](https://vuejs.org)

---

This example page demonstrates how to combine various components with regular Markdown content to create a cohesive and visually appealing page. Feel free to use this as a template for your own pages.
