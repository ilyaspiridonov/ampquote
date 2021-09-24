# Bento Embedly Card

## Behavior

The Bento Embedly Card component provides you with responsive and shareable embeds to drive the reach of your websites,
blog posts, and articles from any URL using [Embedly cards](http://docs.embed.ly/docs/cards). Use it as a web component [`<bento-embedly-card>`](#web-component), or a Preact/React functional component [`<BentoEmbedlyCard>`](#preact/react-Component).

Cards are the easiest way to leverage Embedly. For any media, cards provide a responsive embed with built-in embed analytics.

If you have a paid plan, use the `<bento-embedly-key>` or `<BentoEmbedlyContext.Provider>` component to set your API key. You just need one Bento Embedly key per page to remove Embedly's branding from the cards. Within your page, you can include one or multiple Bento Embedly Card instances.

### Web Component

You must include each Bento component's required CSS library to guarantee proper loading and before adding custom styles. Or use the light-weight pre-upgrade styles available inline. See [Layout and style](#layout-and-style).

The examples below demonstrate use of the `<bento-embedly-card>` web component.

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

The `bento-embedly-card` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children (slides) via a desired CSS layout (such as one defined with `height`, `width`, `aspect-ratio`, or other such properties):



#### Attributes

##### `data-url`

The URL to retrieve embedding information.

##### `data-card-embed`

The URL to a video or rich media. Use with static embeds like articles, instead
of using the static page content in the card, the card will embed the video or
rich media.

##### `data-card-image`

The URL to an image. Specifies which image to use in article cards when
`data-url` points to an article. Not all image URLs are supported, if the image
is not loaded, try a different image or domain.

##### `data-card-controls`

Enables share icons.

-   `0`: Disable share icons.
-   `1`: Enable share icons

The default is `1`.

##### `data-card-align`

Aligns the card. The possible values are `left`, `center` and `right`. The
default value is `center`.

##### `data-card-recommend`

When recommendations are supported, it disables embedly recommendations on video
and rich cards. These are recommendations created by embedly.

-   `0`: Disables embedly recommendations.
-   `1`: Enables embedly recommendations.

The default value is `1`.

##### `data-card-via` (optional)

Specifies the via content in the card. This is a great way to do attribution.

##### `data-card-theme` (optional)

Allows settings the `dark` theme which changes the background color of the main
card container. Use `dark` to set this theme. For dark backgrounds it's better
to specify this. The default is `light`, which sets no background color of the
main card container.

##### title (optional)

Define a `title` attribute for the component to propagate to the underlying `<iframe>` element. The default value is `"Embedly card"`.

### Preact/React Component

The examples below demonstrate use of the `<BentoEmbedlyCard>` as a functional component usable with the Preact or React libraries.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:





[/example]

#### Layout and style

**Container type**

The `BentoEmbedlyCard` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children (slides) via a desired CSS layout (such as one defined with `height`, `width`, `aspect-ratio`, or other such properties). These can be applied inline:



Or via `className`:



### Props

##### `url`

The URL to retrieve embedding information.

##### `cardEmbed`

The URL to a video or rich media. Use with static embeds like articles, instead
of using the static page content in the card, the card will embed the video or
rich media.

##### `cardImage`

The URL to an image. Specifies which image to use in article cards when
`data-url` points to an article. Not all image URLs are supported, if the image
is not loaded, try a different image or domain.

##### `cardControls`

Enables share icons.

-   `0`: Disable share icons.
-   `1`: Enable share icons

The default is `1`.

##### `cardAlign`

Aligns the card. The possible values are `left`, `center` and `right`. The
default value is `center`.

##### `cardRecommend`

When recommendations are supported, it disables embedly recommendations on video
and rich cards. These are recommendations created by embedly.

-   `0`: Disables embedly recommendations.
-   `1`: Enables embedly recommendations.

The default value is `1`.

##### `cardVia` (optional)

Specifies the via content in the card. This is a great way to do attribution.

##### `cardTheme` (optional)

Allows settings the `dark` theme which changes the background color of the main
card container. Use `dark` to set this theme. For dark backgrounds it's better
to specify this. The default is `light`, which sets no background color of the
main card container.

##### title (optional)

Define a `title` attribute for the component to propagate to the underlying `<iframe>` element. The default value is `"Embedly card"`.