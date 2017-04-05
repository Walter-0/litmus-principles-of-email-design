# Litmus - Principles of Email Design

## Email is great because it's:

- Iterative
- Testable
- Personal
- Forgettable

## Email is annoying because:

THERE ARE NO STANDARDS 😂
Always include client-specific styles and resets.

## Preheaders

- Preview text that introduces the email
- Put the text in the first div, and hide it.

## Tables

### <table>

Best practice to set:

```html
<table border="0" cellpadding="0" cellspacing="0" width="100%">
  <!-- Put table rows here -->
</table>
```

For single column layouts, use one container table with `width="100%"` and 1 column table with `width="600"`

### <tr>

Functions as a module (header, footer, paragraph block)

### <td>

Best practice to set:

```html
<td align="center" valign="top" style="padding: 60px 10px 20px 10px">
  <!-- Put content here -->
</td>
```

## Accessibility

Include `role="presentation"` to all tables.
Good idea to keep text **big** and **readable**.

## Text and Semantics

Text should be the primary form of content
Many email clients block images by default
Old way: dump text directly into `<td>`
Best way: use semantic elements **inside** `<td>`

### h1-h6, p, span
Best practice to set:
```html
<h1 style="color: #333333; font-family: sans-serif; font-size: 16px; font-weight: bold; line-height: 20px; margin: 0;"></h1>

<p style="color: #333333; font-family: sans-serif; font-size: 16px; font-weight: bold; line-height: 20px; margin: 0;"></p>

<span style="color: #decade; font-style: italic; font-weight: normal;"></span>
```

## Links and Buttons

### <a>

Regular anchor
Must always use absolute path
Best practice to set:

```html
<a href="https://duckduckgo.com" style="color: lightskyblue; font-weight: bold; text-decoration: underline">DuckDuckGo</a>
```

Don't confuse users. Underline links, don't underline things that aren't links

### button

- Image-based buttons
  - Advanced styles
  - Won't work everywhere
- Bulletproof buttons
  - HTML/CSS
  - Works everywhere!
  - Not a real `<button>`
  - Make a block-level anchor tag, with background colors and borders, etc.
  - [Just use the generator](https://buttons.cm/)

## Images <img>

Best practice to set:

```html
<img src="http://example.com/image.png" width="600" border="0" alt="Image of a tree">
```

Many clients block emails.
Always add alt text.
You can style alt text???

```html
<img src="http://example.com/image.png" width="600" border="0" alt="Image of a tree" style="color: #decade; font-family: sans-serif; font-size: 18px; display: block;">
```

### Make images **responsive by default**

Add `max-width: 100%`, `min-width: MIN_WIDTH`, and `width: 100%`

### 2x DPI images

Use a second, 2x image

Pros:
- Better UI
- Future proof assets

Cons:
- Bigger files, slower loading times
