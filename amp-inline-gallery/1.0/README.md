# Bento Inline Gallery

## Usage

The Bento Inline Gallery component uses a Bento Carousel component to display slides, with optional pagination dots and thumbnails. Both components must be properly installed for the environment (Web Component vs Preact).

### Web Component

You must include each Bento component's required CSS library to guarantee proper loading and before adding custom styles. Or use the light-weight pre-upgrade styles available inline. See [Layout and style](#layout-and-style).

The examples below demonstrate use of the `<bento-inline-gallery>` web component.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:


[/example]

#### Example: Include via `<script>`

The example below contains a `bento-inline-gallery` consisting of three slides with thumbnails and a pagination indicator.

[example preview="top-frame" playground="false"]



[/example]

#### Layout and style

Each Bento component has a small CSS library you must include to guarantee proper loading without [content shifts](https://web.dev/cls/). Because of order-based specificity, you must manually ensure that stylesheets are included before any custom styles.



Alternatively, you may also make the light-weight pre-upgrade styles available inline:



#### Attributes

##### `<bento-inline-gallery-pagination>`

###### `inset`

Default: `false`

Boolean attribute indicating whether to display the pagination indicator as inset (overlaying the carousel itself)

##### `<bento-inline-gallery-thumbnails>`

###### `aspect-ratio`

Optional

Number: ratio of width to height that slides should be displayed in.

###### `loop`

Default: `false`

Boolean attribute indicating whether thumbnails should loop.

#### Styling

You may use the `bento-inline-gallery`, `bento-inline-gallery-pagination`, `bento-inline-gallery-thumbnails`, and `bento-base-carousel` element selectors to style the pagination indicator, thumbnails, and carousel freely.

### Preact/React Component

The examples below demonstrates use of the `<BentoInlineGallery>` as a functional component usable with the Preact or React libraries.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:



[/example]

#### Layout and style

**Container type**

The `BentoInlineGallery` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children via a desired CSS layout (such as one defined with `width`). These can be applied inline:



Or via `className`:



#### Props

##### BentoInlineGallery

##### BentoInlineGalleryPagination

In addition to the [common props](../../../docs/spec/bento-common-props.md), BentoInlineGalleryPagination supports the props below:

###### `inset`

Default: `false`

Boolean attribute indicating whether to display the pagination indicator as inset (overlaying the carousel itself)

##### BentoInlineGalleryThumbnails

In addition to the [common props](../../../docs/spec/bento-common-props.md), BentoInlineGalleryThumbnails supports the props below:

###### `aspectRatio`

Optional

Number: ratio of width to height that slides should be displayed in.

###### `loop`

Default: `false`

Boolean attribute indicating whether thumbnails should loop.
