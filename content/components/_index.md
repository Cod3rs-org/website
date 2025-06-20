---
title: "Design Components"
description: "Documentation for the design components available in the Cod3rs Community website"
draft: true
---

# Design Components

This page showcases the various design components available for use in the Cod3rs Community website. These components provide consistent styling and make it easier to create visually appealing pages.

## Dark Background Components

### 1. Hero Banner - Dark

A full-width banner with dark background for page headers or important announcements.

```html
<div class="component-hero-dark">
  <h1>Your Heading Here</h1>
  <p>Your descriptive text goes here. This component is perfect for page headers or important announcements that need to stand out.</p>
</div>
```

<div class="component-hero-dark">
  <h1>Hero Banner Example</h1>
  <p>This is an example of the Hero Banner component with a dark background. It's perfect for page headers or important announcements that need to stand out.</p>
</div>

### 2. Feature Box - Dark

A box for highlighting features or services with dark background and an accent border on the left.

```html
<div class="component-feature-dark">
  <h3>Feature Title</h3>
  <p>Description of the feature or service that you want to highlight.</p>
</div>
```

<div class="component-feature-dark">
  <h3>Feature Box Example</h3>
  <p>This is an example of the Feature Box component with a dark background. Use it to highlight important features or services.</p>
</div>

### 3. Card - Dark

A card component with dark background for content display.

```html
<div class="component-card-dark">
  <h3>Card Title</h3>
  <p>Card content goes here. This can include descriptions, features, or any other information.</p>
  <a href="#" class="btn">Call to Action</a>
</div>
```

<div class="component-card-dark">
  <h3>Card Example</h3>
  <p>This is an example of the Card component with a dark background. It's perfect for displaying content with a call to action button.</p>
  <a href="#" class="btn">Learn More</a>
</div>

### 4. Split Content - Dark

A two-column layout with dark background for content and image/code.

```html
<div class="component-split-dark">
  <div class="content">
    <h3>Content Title</h3>
    <p>Your text content goes here. This can be a description, explanation, or any other text-based content.</p>
  </div>
  <div class="media">
    <img src="/path/to/image.jpg" alt="Description">
    <!-- Or you can use code snippets -->
    <!-- <pre><code>Your code here</code></pre> -->
  </div>
</div>
```

<div class="component-split-dark">
  <div class="content">
    <h3>Split Content Example</h3>
    <p>This is an example of the Split Content component with a dark background. It's perfect for displaying content alongside images or code snippets.</p>
  </div>
  <div class="media">
    <img src="/img/logo.png" alt="Cod3rs Logo">
  </div>
</div>

### 5. Call to Action - Dark

A call to action component with dark background.

```html
<div class="component-cta-dark">
  <h2>Call to Action Title</h2>
  <p>Your call to action text goes here. Make it compelling and clear about what action you want the user to take.</p>
  <a href="#" class="btn">Take Action</a>
</div>
```

<div class="component-cta-dark">
  <h2>Join Our Community</h2>
  <p>Become a part of our growing community and start your journey with us. Whether you're a beginner or an experienced developer, there's a place for you here.</p>
  <a href="/contact/" class="btn">Get Started</a>
</div>

## White Background Components

### 6. Info Box - White

An information box with white background.

```html
<div class="component-info-white">
  <h3>Information Title</h3>
  <p>Your information text goes here. This can include important details, explanations, or any other information you want to highlight.</p>
  <p>You can also use the <span class="accent">accent</span> class to highlight specific text.</p>
</div>
```

<div class="component-info-white">
  <h3>Info Box Example</h3>
  <p>This is an example of the Info Box component with a white background. It's perfect for displaying important information or explanations.</p>
  <p>You can also use the <span class="accent">accent</span> class to highlight specific text.</p>
</div>

### 7. Timeline - White

A timeline component with white background for displaying chronological events.

```html
<div class="component-timeline-white">
  <h3>Timeline Title</h3>
  
  <div class="timeline-item">
    <div class="timeline-date">Date or Time Period</div>
    <div class="timeline-content">
      <h4>Event Title</h4>
      <p>Description of the event or milestone.</p>
    </div>
  </div>
  
  <div class="timeline-item">
    <div class="timeline-date">Another Date</div>
    <div class="timeline-content">
      <h4>Another Event</h4>
      <p>Description of another event or milestone.</p>
    </div>
  </div>
</div>
```

<div class="component-timeline-white">
  <h3>Community Timeline</h3>
  
  <div class="timeline-item">
    <div class="timeline-date">January 2023</div>
    <div class="timeline-content">
      <h4>Community Founded</h4>
      <p>The Cod3rs Community was officially founded with the goal of bringing together passionate developers.</p>
    </div>
  </div>
  
  <div class="timeline-item">
    <div class="timeline-date">March 2023</div>
    <div class="timeline-content">
      <h4>First Meetup</h4>
      <p>We held our first community meetup with over 50 attendees.</p>
    </div>
  </div>
</div>

## Purple Background Component

### 8. Highlight Box - Purple

A highlight box with purple background for important content.

```html
<div class="component-highlight-purple">
  <h3>Highlight Title</h3>
  <p>Your highlighted content goes here. This component is perfect for content that needs to really stand out on the page.</p>
  <a href="#" class="btn">Call to Action</a>
</div>
```

<div class="component-highlight-purple">
  <h3>Highlight Box Example</h3>
  <p>This is an example of the Highlight Box component with a purple background. It's perfect for content that needs to really stand out on the page.</p>
  <a href="#" class="btn">Learn More</a>
</div>

## Using Components in Markdown

When creating content in Markdown files, you can include these components by using HTML directly in your Markdown files. Hugo will render the HTML as expected.

For example:

```markdown
# My Page Title

Regular markdown content goes here.

<div class="component-hero-dark">
  <h1>Hero Section</h1>
  <p>This is a hero section created using the component-hero-dark class.</p>
</div>

More markdown content...
```

## Responsive Behavior

All components are designed to be responsive and will adapt to different screen sizes. On mobile devices, the two-column layouts will stack vertically, and font sizes will be adjusted for better readability.