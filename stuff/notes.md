# Applied Accessibility

## Add a Text Alternative to Images for Visually Impaired Accessibility

- `alt` attributes are now mandatory according to HTML5 spec for images
- Sometimes `alt` text can be left blank if the images are grouped with a caption describing them, or if they are for decoration only (e.g. background image)
- Set the `alt` attribute to be an empty string instead, e.g. `<img src="visualDecoration.jpeg" alt="">
- For images with a caption you may still want to include `alt` text so it can be read by search engines

## Use Headings to Show Hierarchical Relationships of Content

- Headings `h1` to `h6` should have semantic meaning and related to each other - not just be picked for their size values - sizing can be changed via CSS if needs be
- For example, a `h2` followed by several subsections labelled with `h4` would confuse a screen reader user
- Each page should only have one `h1` which should be the main subject of your content and is used by search engines to understand content

## New Elements Introduced by HTML5

- HTML5 introduced new elements, including `main`, `header`, `footer`, `nav`, `article`, `section` among others
- These elements are rendered similarly to a `div` but they allow for greater clarity and accessibility
- `main` is used to wrap the main page content and there should only be one per page. It should surround the information that's related to the central topic of your page, not including things that repeat across pages, such as navs or banners
- `main` also has an embedded landmark feature than enable assistive technologies to "jump straight to main content"
- `article` is also a sectioning element, used to wrap independent, self-contained content. It works well with blog posts, forum posts or news articles
- `section` is used for grouping thematically related content and can be used alongside `article`. If a book is the `article` then a chapter is a `section`. If there's no relationship between groups of content, then a `div` can be used
    - `div` - groups content
    - `section` - groups related content
    - `article` - groups independent, self-contained content
- `header` is used to wrap introductory information or navigation links for its parent tag and is good around content that is repeated across pages. It also shares the same embedded landmark feature, allowing assistive technologies to quickly jump to it. It is designed for use inside the `body` tag and is different to the `head` element
- `nav` is designed to wrap around the main navigational links on your page. If the links are repeated at the bottom, you don't need to mark those up with `nav` as well. Using a `footer` is enough. It also features the embedded landmark function.
- `footer` also an embedded landmark feature. It's usually used to contain copyright information or links to related documents that usually sit at the bottom of a page
- `audio` is used to indicate sound or audio stream content. It needs a text alternative to be accessible, either as nearby text on the page or with a link to a transcript. It also supports the `controls` attribute which brings up browser play/pause and other controls. It doesn't need a value as a boolean attribute - its mere presence is enough
```
<audio id="meowClip" controls>
  <source src="audio/meow.mp3" type="audio/mpeg" />
  <source src="audio/meow.ogg" type="audio/ogg" />
</audio>
```
- 