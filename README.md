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

Nothing to see here

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
