---
title: "Section Components"
description: "Documentation for the section shortcodes available in the Cod3rs Community website"
draft: true
---

# Section Components

This page documents the various section shortcodes available for use in the Cod3rs Community website. These shortcodes provide flexible layout options and make it easier to create visually appealing pages.

## Basic Section

The basic section shortcode creates a simple section with customizable class, style, and ID attributes.

```markdown
{{</* section class="custom-class" style="padding: 3rem 0;" id="section-id" */>}}
## Section Title

This is the content of the section. You can include any Markdown content here.

- List item 1
- List item 2
- List item 3
{{</* /section */>}}
```

## Full-Width Section

The full-width section shortcode creates a section that spans the full width of the page.

```markdown
{{</* section-full class="custom-class" style="background-color: #f5f5f5;" id="full-width-section" */>}}
## Full-Width Section

This section spans the full width of the page. The content is centered and has a maximum width.
{{</* /section-full */>}}
```

## Two-Column Section

The two-column section shortcode creates a section with content split into two columns. Use the `column` shortcode inside it to define each column.

```markdown
{{</* section-two-column class="custom-class" style="padding: 3rem 0;" id="two-column-section" */>}}
{{</* column class="custom-column-class" style="padding: 2rem;" */>}}
## Left Column

Content for the left column goes here.
{{</* /column */>}}

{{</* column class="custom-column-class" style="padding: 2rem;" */>}}
## Right Column

Content for the right column goes here.
{{</* /column */>}}
{{</* /section-two-column */>}}
```

## Dark Section

The dark section shortcode creates a section with a dark background and light text.

```markdown
{{</* section-dark class="custom-class" style="padding: 3rem 0;" id="dark-section" */>}}
## Dark Section

This section has a dark background and light text.
{{</* /section-dark */>}}
```

## Light Section

The light section shortcode creates a section with a light background and dark text.

```markdown
{{</* section-light class="custom-class" style="padding: 3rem 0;" id="light-section" */>}}
## Light Section

This section has a light background and dark text.
{{</* /section-light */>}}
```

## Accent Section

The accent section shortcode creates a section with an accent (purple) background and light text.

```markdown
{{</* section-accent class="custom-class" style="padding: 3rem 0;" id="accent-section" */>}}
## Accent Section

This section has an accent (purple) background and light text.
{{</* /section-accent */>}}
```

## Section with Background Image

The section-image shortcode creates a section with a background image and overlay.

```markdown
{{</* section-image class="custom-class" style="padding: 5rem 0;" id="image-section" image="/path/to/image.jpg" */>}}
## Section with Background Image

This section has a background image with a dark overlay.
{{</* /section-image */>}}
```

## Card with Image

The card-image shortcode creates a card with an image, title, and content.

```markdown
{{</* card-image class="custom-class" style="max-width: 400px;" id="card-id" image="/path/to/image.jpg" alt="Image description" title="Card Title" */>}}
This is the content of the card. You can include any Markdown content here.

[Learn More](#)
{{</* /card-image */>}}
```

## Hero Section with Image

The hero-image shortcode creates a hero section with a background image, overlay, title, and subtitle.

```markdown
{{</* hero-image class="custom-class" style="height: 80vh;" id="hero-id" image="/path/to/image.jpg" overlayColor="rgba(0, 0, 0, 0.7)" textColor="white" title="Hero Title" subtitle="Hero Subtitle" */>}}
This is the content of the hero section. You can include any Markdown content here.

[Get Started](#){.btn .btn-primary}
{{</* /hero-image */>}}
```

## Example Page

Here's an example of how to use these section components together to create a complete page:

```markdown
---
title: "Example Page"
description: "An example page using section components"
---

{{</* hero-image image="/img/hero-bg.jpg" title="Welcome to Our Website" subtitle="Discover our services and products" */>}}
[Get Started](#services){.btn .btn-primary}
{{</* /hero-image */>}}

{{</* section-full class="intro-section" id="intro" */>}}
## About Us

We are a company dedicated to providing high-quality services and products.
{{</* /section-full */>}}

{{</* section-two-column id="services" */>}}
{{</* column */>}}
## Our Services

- Service 1
- Service 2
- Service 3
{{</* /column */>}}

{{</* column */>}}
## Our Products

- Product 1
- Product 2
- Product 3
{{</* /column */>}}
{{</* /section-two-column */>}}

{{</* section-dark id="testimonials" */>}}
## Testimonials

> "This company provides excellent services!" - John Doe
{{</* /section-dark */>}}

{{</* section-accent id="contact" */>}}
## Contact Us

Email us at info@example.com or call us at 123-456-7890.
{{</* /section-accent */>}}
```

## Customization

All section shortcodes support the following attributes:

- `class`: Additional CSS classes to apply to the section
- `style`: Inline CSS styles to apply to the section
- `id`: HTML ID attribute for the section

Some shortcodes support additional attributes, as shown in the examples above.