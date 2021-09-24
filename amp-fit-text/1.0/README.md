# Bento Fit Text

## Usage

Expands or shrinks its font size to fit the content within the space given to it. Use Bento Fit Text as a web component [`<bento-fit-text>`](#web-component), or a Preact/React functional component [`<BentoFitText>`](#preact/react-Component).

The Bento Fit Text component allows you to manage the size and fit of text within a specified area. For content contained in a Bento Fit Text component, it determines the best font size to fit all of the content within the available space. The expected content for Bento Fit Text is text or other inline content, but it can also contain non-inline content.

### Web Component

You must include each Bento component's required CSS library to guarantee proper loading and before adding custom styles. Or use the light-weight pre-upgrade styles available inline. See [Layout and style](#layout-and-style).

The examples below demonstrate use of the `<bento-fit-text>` web component.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:



[/example]

#### Example: Include via `<script>`

[example preview="top-frame" playground="false"]



[/example]

#### Overflowing content

If the content of the `bento-fit-text` overflows the available space, even with a
`min-font-size` specified, the overflowing content is cut off and hidden. WebKit and Blink-based browsers show ellipsis for overflowing content.

In the following example, we specified a `min-font-size` of `40`, and added more content inside the `bento-fit-text` element. This causes the content to exceed the size of its fixed block parent, so the text is truncated to fit the container.

[example preview="inline" playground="true" imports="bento-fit-text:1.0"]



[/example]

#### Layout and style

Each Bento component has a small CSS library you must include to guarantee proper loading without [content shifts](https://web.dev/cls/). Because of order-based specificity, you must manually ensure that stylesheets are included before any custom styles.



Alternatively, you may also make the light-weight pre-upgrade styles available inline:


**Container type**

The `bento-fit-text` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children (slides) via a desired CSS layout (such as one defined with `height`, `width`, `aspect-ratio`, or other such properties):



#### Accessibility considerations of overflowing content

While overflowing content is _visually_ truncated to fit the container, note that it's still present in the document. Do not rely on the overflow behaviour to simply "stuff" large amounts of content in your pages - while visually it may look appropriate, it may lead to the page becoming overly verbose to users of assistive technologies (such as screen readers), as for these users all the truncated content will still be read/announced in full.

#### Attributes

##### Media Queries

The attributes for `<bento-fit-text>` can be configured to use different
options based on a [media query](./../../../docs/spec/amp-html-responsive-attributes.md).

##### `min-font-size`

Specifies the minimum font size in pixels as an integer that the `bento-fit-text` can use.

##### `max-font-size`

Specifies the maximum font size in pixels as an integer that the `bento-fit-text` can use.

### Preact/React Component

The examples below demonstrate use of the `<BentoFitText>` as a functional component usable with the Preact or React libraries.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:



[/example]

#### Layout and style

**Container type**

The `BentoFitText` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children (slides) via a desired CSS layout (such as one defined with `height`, `width`, `aspect-ratio`, or other such properties). These can be applied inline:


Or via `className`:





#### Props

##### `minFontSize`

Specifies the minimum font size in pixels as an integer that the `bento-fit-text` can use.

##### `maxFontSize`

Specifies the maximum font size in pixels as an integer that the `bento-fit-text` can use.
