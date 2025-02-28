# Meta data in HTML

Meta data in HTML provides important information about a webpage, helping search engines, social media, and browsers understand the content. It is added inside the `<head>` section of an HTML document.

## Why meta data matters
- Helps search engines **understand** your webpage.
- Improves **SEO rankings**.
- Controls how pages appear on **social media**.
- Defines character sets and viewport settings for **better user experience**.

## Common meta tags

### 1. **Title Tag**
Defines the title of the page, shown in browser tabs and search results.

```html
<title>My Awesome Website</title>
```

### 2. **Meta Description**
A short summary of the webpage, often displayed in search engine results.

```html
<meta name="description" content="Learn how to use HTML meta tags to improve SEO and user experience.">
```

### 3. **Meta Keywords** *(Rarely used today)*
Used to contain keywords related to the content but is no longer important for SEO.

```html
<meta name="keywords" content="HTML, meta tags, SEO, web development">
```

### 4. **Viewport Meta Tag** *(For Responsive Design)*
Ensures the page scales properly on mobile devices.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### 5. **Character Encoding**
Defines the character set for the webpage to avoid display issues.

```html
<meta charset="UTF-8">
```

## Social media meta tags

### 6. **Open Graph (OG) Tags** *(For Facebook, LinkedIn, etc.)*
Improve how the webpage appears when shared on social media.

```html
<meta property="og:title" content="My Awesome Website">
<meta property="og:description" content="Learn about HTML meta tags!">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:url" content="https://example.com">
```

### 7. **Twitter Card Tags** *(For Twitter Sharing)*
Customize the way links appear on Twitter.

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="My Awesome Website">
<meta name="twitter:description" content="Learn about HTML meta tags!">
<meta name="twitter:image" content="https://example.com/image.jpg">
```

## Robots Meta Tag *(For Search Engines)*
Control how search engines index and follow links on a page.

```html
<meta name="robots" content="index, follow">
```
- `index, follow` → Allow indexing and following links.
- `noindex, nofollow` → Prevent search engines from indexing and following links.

## Refresh & Redirect meta tag *(Use With Caution)*
Automatically refreshes or redirects a page after a set time.

```html
<meta http-equiv="refresh" content="5; url=https://newpage.com">
```
- Redirects to "newpage.com" after **5 seconds**.

