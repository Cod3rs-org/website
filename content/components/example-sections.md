---
title: "Section Components Example"
description: "An example page demonstrating the use of section shortcodes"
draft: true
---

# Section Components Example

This page demonstrates how to use the section shortcodes in a real-world scenario. It shows how different section components can be combined to create a cohesive and visually appealing page.

## Hero Image

{{< hero-image image="/img/large-logo-bg.png" title="Welcome to Our Workshop" subtitle="Learn how to use section components effectively" >}}
[Get Started](#basic-section){.btn .btn-primary}
{{< /hero-image >}}

<hr>

```markdown
{{</* hero-image image="/path/to/image.jpg" title="Hero Title" subtitle="Hero Subtitle" */>}}
[Get Started](#){.btn .btn-primary}
{{</* /hero-image */>}}
```

## Basic Section

{{< section id="basic-section" >}}
## Basic Section

This is a basic section created with the `section` shortcode. It has default styling and can contain any Markdown content.

- You can include lists
- Format text as **bold** or *italic*
- Add [links](#) and other Markdown elements

The basic section is the foundation for all other section types.
{{< /section >}}

<hr>

```markdown
{{</* section class="custom-class" style="padding: 3rem 0;" id="section-id" */>}}
## Section Title

This is the content of the section. You can include any Markdown content here.

- List item 1
- List item 2
- List item 3
{{</* /section */>}}
```

{{< section-full class="bg-light" id="full-width-section" >}}
## Full-Width Section

This section spans the full width of the page. It's perfect for content that needs to stand out or for creating visual breaks between other sections.

The content is centered and has a maximum width to ensure readability on large screens.
{{< /section-full >}}

<hr>

```markdown
{{</* section-full class="custom-class" style="background-color: #f5f5f5;" id="full-width-section" */>}}
## Full-Width Section

This section spans the full width of the page. The content is centered and has a maximum width.
{{</* /section-full */>}}
```

{{< section-two-column id="two-column-section" >}}
{{< column >}}
## Left Column

This is the content for the left column. The two-column layout is great for:

- Comparing features
- Showing before/after scenarios
- Presenting related but distinct content
- Creating more interesting layouts

You can customize each column independently.
{{< /column >}}

{{< column >}}
## Right Column

This is the content for the right column. On mobile devices, these columns will stack vertically to ensure good readability.

The two-column section is responsive and will adjust based on the screen size. You can also customize the width of each column if needed.
{{< /column >}}
{{< /section-two-column >}}

<hr>

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

{{< section-dark id="dark-section" >}}
## Dark Section

This section has a dark background with light text. It's perfect for creating visual contrast on your page and highlighting important content.

> Dark sections can be particularly effective for testimonials, calls to action, or important announcements.

The dark background helps this content stand out from the rest of the page.
{{< /section-dark >}}

<hr>

```markdown
{{</* section-dark class="custom-class" style="padding: 3rem 0;" id="dark-section" */>}}
## Dark Section

This section has a dark background and light text.
{{</* /section-dark */>}}
```

{{< section-light id="light-section" >}}
## Light Section

This section has a light background with dark text. It's the most traditional section style and is great for most content.

The light background provides good readability for longer text content and is easy on the eyes.
{{< /section-light >}}

<hr>

```markdown
{{</* section-light class="custom-class" style="padding: 3rem 0;" id="light-section" */>}}
## Light Section

This section has a light background and dark text.
{{</* /section-light */>}}
```

{{< section-accent id="accent-section" >}}
## Accent Section

This section has an accent (purple) background with light text. It's perfect for highlighting special content or calls to action.

The accent color draws attention to this section and makes it stand out from the rest of the page.
{{< /section-accent >}}

<hr>

```markdown
{{</* section-accent class="custom-class" style="padding: 3rem 0;" id="accent-section" */>}}
## Accent Section

This section has an accent (purple) background and light text.
{{</* /section-accent */>}}
```

{{< section-image image="/img/large-logo-bg.png" id="image-section" >}}
## Section with Background Image

This section has a background image with a dark overlay. It's perfect for creating visually appealing sections with text overlay.

The dark overlay ensures that the text remains readable regardless of the background image.
{{< /section-image >}}

<hr>

```markdown
{{</* section-image class="custom-class" style="padding: 5rem 0;" id="image-section" image="/path/to/image.jpg" */>}}
## Section with Background Image

This section has a background image with a dark overlay.
{{</* /section-image */>}}
```

{{< section id="cards-section" >}}
## Cards with Images

Cards are great for displaying content in a structured and visually appealing way. Here are some examples:
{{< /section >}}

{{< card-image image="/img/logo.png" title="Card Title 1" >}}
This is a card with an image. Cards are perfect for displaying products, services, team members, or any content that benefits from a visual element.

[Learn More](#)
{{< /card-image >}}

{{< card-image image="/img/logo.png" title="Card Title 2" >}}
You can create multiple cards and arrange them in a grid or list. Each card can have its own image, title, and content.

[Learn More](#)
{{< /card-image >}}

<hr>

```markdown
{{</* card-image class="custom-class" style="max-width: 400px;" id="card-id" image="/path/to/image.jpg" alt="Image description" title="Card Title" */>}}
This is the content of the card. You can include any Markdown content here.

[Learn More](#)
{{</* /card-image */>}}
```

{{< section-dark id="conclusion" >}}
## Conclusion

As you can see, section components provide a flexible and powerful way to structure your content. By combining different section types, you can create visually appealing and well-organized pages.

Experiment with different combinations to find what works best for your content!
{{< /section-dark >}}
