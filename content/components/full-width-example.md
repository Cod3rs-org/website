---
title: "Full Width Example"
description: "An example page demonstrating the fullWidth parameter"
fullWidth: true
---

# Full Width Example

This page demonstrates the use of the `fullWidth: true` parameter in the frontmatter. Unlike regular pages that have their content wrapped in a container with a maximum width of 1200px, this page's content spans the full width of the browser window.

## How to Implement Full Width

To make a page use the full width of the browser window, add the following parameter to the page's frontmatter:

```yaml
---
title: "Your Page Title"
description: "Your page description"
fullWidth: true
---
```

This parameter tells the template to render the page without the container that normally limits the content width.

## When to Use Full Width

The full width layout is useful for:

1. Pages with large tables that need more horizontal space
2. Galleries or image collections that benefit from using the entire screen
3. Custom layouts where you want to control the width yourself
4. Data visualization or charts that need more space

## Comparison

To see the difference, compare this page with the [Design Components](/components/) page, which uses the default container layout.

## Example of Wide Content

{{< rawhtml >}}
<div style="overflow-x: auto;">
  <table style="width: 100%; border-collapse: collapse; border: 2px solid #212121;">
    <thead>
      <tr style="background-color: #212121; color: white;">
        <th style="padding: 10px; text-align: left;">Column 1</th>
        <th style="padding: 10px; text-align: left;">Column 2</th>
        <th style="padding: 10px; text-align: left;">Column 3</th>
        <th style="padding: 10px; text-align: left;">Column 4</th>
        <th style="padding: 10px; text-align: left;">Column 5</th>
        <th style="padding: 10px; text-align: left;">Column 6</th>
        <th style="padding: 10px; text-align: left;">Column 7</th>
        <th style="padding: 10px; text-align: left;">Column 8</th>
        <th style="padding: 10px; text-align: left;">Column 9</th>
        <th style="padding: 10px; text-align: left;">Column 10</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 1</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 2</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 3</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 4</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 5</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 6</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 7</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 8</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 9</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 10</td>
      </tr>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 11</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 12</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 13</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 14</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 15</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 16</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 17</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 18</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 19</td>
        <td style="padding: 10px; border: 1px solid #ddd;">Data 20</td>
      </tr>
    </tbody>
  </table>
</div>
{{< /rawhtml >}}
