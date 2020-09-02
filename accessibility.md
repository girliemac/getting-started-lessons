# Creating accessible webpages

> The power of the Web is in its universality. Access by everyone regardless of disability is an essential aspect.
>
> \- Tim Berners-Lee, W3C Director and inventor of the World Wide Web

Tim perfectly highlights the importance of creating accessible websites. An application which can't be accessed by all is by definition exclusionary. As web developers we should always have accessibility in mind. By having this focus from the beginning you will be well on your way to ensure everyone can access the pages you create.

## Screen readers

[Screen readers](https://en.wikipedia.org/wiki/Screen_reader) are commonly used clients for those with vision impairments. Just as we spend time ensuring a browser properly conveys the information we wish to share, we must also ensure a screen reader does the same.

At its most basic, a screen reader will read a page from top to bottom. If your page is all text, the reader will convey the information in a similar fashion to a browser. Of course, web pages are rarely purely text; they will contain links, graphics, color, and other visual components. Care must be taken to ensure our information is read correctly by a screen reader.

Every web developer should familiarize themselves with a screen reader. As highlighted above, it's the client your users will utilize. Much in the same way you're familiar with how a browser operates, you should learn how a screen reader operates. Fortunately screen readers are built into most operating systems, and many browsers contain extensions to emulate a screen reader.

## Designing for accessibility

Accessibility is a relatively large topic. To help you out, there are numerous resources available.

- [Accessible U - University of Minnesota](https://accessibility.umn.edu/your-role/web-developers)

While we won't be able to cover every aspect of creating accessible sites, below are some of the core tenants you will want to implement. Designing an accessible page from the start is **always** easier than going back to an existing page to make it accessible.

## Good display principles

### Color safe palettes

People see the world in different ways, and this includes colors. When selecting a color scheme for your site, you should ensure it's accessible to all. One great [tool for generating color palettes is Color Safe](http://colorsafe.co/).

### Properly highlight text

Highlighting text by color, [font weight](https://developer.mozilla.org/docs/Web/CSS/font-weight), or other [text decoration](https://developer.mozilla.org/docs/Web/CSS/text-decoration) does not inherently inform a screen reader of its importance. A word could be bold because it's a key word, or simply because its the first word and the designer decided it should be bold.

When a particular phrase needs to be highlighted, use the `<strong>` or `<em>` elements. These will indicate to a screen reader those items are important.

### Use the correct HTML

With CSS and JavaScript it's possible to many any element look like any type of control. `<span>` could be used to create a `<button>`, and `<b>` could become a hyperlink. While this might be cute, it's baffling to a screen reader. Use the appropriate HTML when creating controls on a page. If you want a hyperlink, use `<a>`.

### Use good visual clues

CSS offers complete control over the look of any element on a page. You can create text boxes without an outline or hyperlinks without an underline. Unfortunately removing those clues can make it more challenging for someone who depends on them to be able to recognize the type of control.

## The importance of link text

Hyperlinks are core to navigating the web. As a result, ensuring a screen reader can properly read links allows all users to navigate your site.

### Screen readers and links

As you would expect, screen readers read link text in the same way they'd read any other text on the page. With this in mind, the text demonstrated below might feel perfectly acceptable.

> The little penguin, sometimes known as the fairy penguin, is the smallest penguin in the world. [Click here](https://en.wikipedia.org/wiki/Little_penguin) for more information.

> The little penguin, sometimes known as the fairy penguin, is the smallest penguin in the world. Visit https://en.wikipedia.org/wiki/Little_penguin for more information.

> **NOTE** As you're about to read, you should **never** create links which look like the above.

Remember, screen readers are a different interface from browsers with a different set of features.

### The problem with using the URL

Screen readers read the text. If a URL appears in the text, the screen reader will read the URL. Generally speaking, the URL does not convey meaningful information, and just sounds annoying. You may have experienced this if your phone has ever audibly read a text message with a URL.

### The problem with "click here"

Screen readers also have the ability to read just the hyperlinks on a page, much in the same way a sighted person would scan a page for links. If the link text is always "click here", all the user will hear is "click here, click here, click here, click here, click here, ..." All links are now indistinguishable from one another.

### Good link text

Good link text briefly describes what's on the other side of the link. In the above example talking about little penguins, the link is to the Wikipedia page about the species. The phrase *little penguins* would make for perfect link text as it makes it clear what someone will learn about if they click the link - little penguins.

> The [little penguin](https://en.wikipedia.org/wiki/Little_penguin), sometimes known as the fairy penguin, is the smallest penguin in the world.

#### Search engine notes

As an added bonus for ensuring your site is accessible to all, you'll help search engines navigate your site as well. Search engines use link text to learn the topics of pages. So using good link text helps everyone!

### Managing duplicated titles

Imagine the following page:

| Product | Description | Order |
| ------- | ------- | ------- |
| Widget | [Description]('#') | [Order]('#') |
| Super widget | [Description]('#') | [Order]('#') |

In this example, duplicating the text of description and order make sense for someone using a browser. However, someone using a screen reader would only hear the words *description* and *order* repeated without context.

To support these types of scenarios, HTML supports a set of attributes known as [Accessible Rich Internet Applications (ARIA)](https://developer.mozilla.org/docs/Web/Accessibility/ARIA). These attributes allow you to provide additional information to screen readers.

> **NOTE**: Like many aspects of HTML, browser and screen reader support may vary. However, most mainline clients support ARIA attributes.

You can use `aria-label` to describe the link when the format of the page doesn't allow you to. The description for widget could be set as

``` html
<a href="#" aria-label="Widget description">description</a>
```

## Images

It goes without saying screen readers are unable to automatically read what's in an image. Ensuring images are accessible doesn't take much work - it's what the `alt` attribute is all about. All images should have an `alt` to describe what they are.

### Search engine notes

As you might expect, search engines are also unable to understand what's in an image. They also use alt text. So once again, ensuring your page is accessible provides additional bonuses!

## Summary

A web accessible to some is a web accessible to none. The best way to ensure the sites you create are accessible is to incorporate the design from the start. While there are extra steps involved, incorporating these skills into your workflow now will mean all pages you create will be accessible.

> Author: Christopher Harrison
