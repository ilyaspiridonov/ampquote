# Bento Wordpress Embed

## Usage

An iframe displaying the [excerpt](https://make.wordpress.org/core/2015/10/28/new-embeds-feature-in-wordpress-4-4/) of a WordPress post or page. Use Bento Wordpress Embed as a web component [`<bento-wordpress-embed>`](#web-component), or a Preact/React functional component [`<BentoWordPressEmbed>`](#preact/react-Component).

### Web Component

You must include each Bento component's required CSS library to guarantee proper loading and before adding custom styles. Or use the light-weight pre-upgrade styles available inline. See [Layout and style](#layout-and-style).

The examples below demonstrate use of the `<bento-wordpress-embed>` web component.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:



[/example]

#### Example: Include via `<script>`

[example preview="top-frame" playground="false"]



[/example]

#### Layout and style

Each Bento component has a small CSS library you must include to guarantee proper loading without [content shifts](https://web.dev/cls/). Because of order-based specificity, you must manually ensure that stylesheets are included before any custom styles.



Alternatively, you may also make the light-weight pre-upgrade styles available inline:



**Container type**

The `bento-wordpress-embed` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children (slides) via a desired CSS layout (such as one defined with `height`, `width`, `aspect-ratio`, or other such properties):


#### Attributes

##### data-url (required)

The URL of the post to embed.

### Preact/React Component

The examples below demonstrate use of the `<BentoWordPressEmbed>` as a functional component usable with the Preact or React libraries.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:



[/example]

#### Layout and style

**Container type**

The `BentoWordPressEmbed` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children (slides) via a desired CSS layout (such as one defined with `height`, `width`, `aspect-ratio`, or other such properties). These can be applied inline:



Or via `className`:



#### Props

##### url (required)

The URL of the post to embed.
