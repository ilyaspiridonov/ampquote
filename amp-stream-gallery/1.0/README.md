# Bento Stream Gallery

## Usage

The Bento Stream Gallery is for displaying multiple similar pieces of content at a time along a horizontal axis. To implement a more customized UX, see
[`bento-base-carousel`](../../amp-base-carousel/1.0/README.md).

Use Bento Stream Gallery as a web component ([`<bento-stream-gallery>`](#web-component)), or a Preact/React functional component ([`<BentoStreamGallery>`](#preact/react-component)).

### Web Component

You must include each Bento component's required CSS library to guarantee proper loading and before adding custom styles. Or use the light-weight pre-upgrade styles available inline. See [Layout and style](#layout-and-style).

The examples below demonstrate use of the `<bento-stream-gallery>` web component.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:



[/example]

#### Example: Include via `<script>`

The example below contains an `bento-stream-gallery` with three sections. The
`expanded` attribute on the third section expands it on page load.

[example preview="top-frame" playground="false"]



[/example]

#### Interactivity and API usage

Bento enabled components in standalone use are highly interactive through their API. The `bento-stream-gallery` component API is accessible by including the following script tag in your document:


##### Actions

**next()**

Moves the carousel forwards by number of slides visible.



**prev()**

Moves the carousel backwards by number of slides visible.



**goToSlide(index: number)**

Moves the carousel to the slide specified by the `index` argument.
Note: `index` will be normalized to a number greater than or equal to `0` and less than the number of slides given.



##### Events

The Bento Stream Gallery component allows you to register and respond to the following events:

**slideChange**

This event is triggered when the index displayed by the carousel has changed.
The new index is available via `event.data.index`.



#### Layout and style

Each Bento component has a small CSS library you must include to guarantee proper loading without [content shifts](https://web.dev/cls/). Because of order-based specificity, you must manually ensure that stylesheets are included before any custom styles.



Alternatively, you may also make the light-weight pre-upgrade styles available inline:



#### Attributes

##### Behavior

###### `controls`

Either `"always"`, `"auto"`, or `"never"`, defaults to `"auto"`. This determines if and when prev/next navigational arrows are displayed. Note: When `outset-arrows` is `true`, the arrows are shown `"always"`.

-   `always`: Arrows are always displayed.
-   `auto`: Arrows are displayed when the carousel has most recently received interaction via mouse, and not displayed when the carousel has most recently received interaction via touch. On first load for touch devices, arrows are displayed until first interaction.
-   `never`: Arrows are never displayed.

###### `extra-space`

Either `"around"` or undefined. This determines how extra space is allocated after displaying the calculated number of visible slides in the carousel. If `"around"`, white space is evenly distributed around the carousel with `justify-content: center`; otherwise, space is allocated to the right of the carousel for LTR documents and to the left for RTL documents.

###### `loop`

Either `true` or `false`, defaults to `true`. When true, the carousel will allow
the user to move from the first item back to the last item and visa versa. There
must be at least three slides present for looping to occur.

###### `outset-arrows`

Either `true` or `false`, defaults to `false`. When true, the carousel will display its arrows outset and on either side of the slides. Note that with outset arrows, the slide container will have an effective length of 100px less than the allotted space for its given container - 50px per arrow on either side. When false, the carousel will display its arrows inset and overlayed on top of the left and right edges of the slides.

###### `peek`

A number, defaults to `0`. This determines how much of an additional slide to show (on one or both sides of the current slide) as an affordance to the user indicating the carousel is swipeable.

##### Gallery slide visibility

###### `min-visible-count`

A number, defaults to `1`. Determines the minimum number of slides that should be shown at a given time. Fractional values can be used to make part of a(n) additional slide(s)
visible.

###### `max-visible-count`

A number, defaults to [`Number.MAX_VALUE`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_VALUE). Determines the maximum number of slides that should be shown at a given time. Fractional values can be used to make part of a(n) additional slide(s) visible.

###### `min-item-width`

A number, defaults to `1`. Determines the minimum width of each item, used to resolve how many whole items can be shown at once within the overall width of the gallery.

###### `max-item-width`

A number, defaults to [`Number.MAX_VALUE`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_VALUE). Determines the maximum width of each item, used to resolve how many whole items can be shown at once within the overall width of the gallery.

##### Slide snapping

###### `slide-align`

Either `start` or `center`. When start aligning, the start of a slide (e.g. the
left edge, when horizontal aligning) is aligned with the start of a carousel.
When center aligning, the center of a slide is aligned with the center of a
carousel.

###### `snap`

Either `true` or `false`, defaults to `true`. Determines whether or not the
carousel should snap on slides when scrolling.

#### Styling

You may use the `bento-stream-gallery` element selector to style the streamGallery
freely.

### Preact/React Component

The examples below demonstrates use of the `<BentoStreamGallery>` as a functional component usable with the Preact or React libraries.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:



[/example]

#### Interactivity and API usage

Bento components are highly interactive through their API. The `BentoStreamGallery` component API is accessible by passing a `ref`:



##### Actions

The `BentoStreamGallery` API allows you to perform the following actions:

**next()**

Moves the carousel forwards by `advanceCount` slides.



**prev()**

Moves the carousel backwards by `advanceCount` slides.


**goToSlide(index: number)**

Moves the carousel to the slide specified by the `index` argument.
Note: `index` will be normalized to a number greater than or equal to `0` and less than the number of slides given.

##### Events

**onSlideChange**

This event is triggered when the index displayed by the carousel has changed.


#### Layout and style

**Container type**

The `BentoStreamGallery` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children via a desired CSS layout (such as one defined with `width`). These can be applied inline:


Or via `className`:



#### Props

##### Common props

This component supports the [common props](../../../docs/spec/bento-common-props.md) for React and Preact components.

##### Behavior

###### `controls`

Either `"always"`, `"auto"`, or `"never"`, defaults to `"auto"`. This determines if and when prev/next navigational arrows are displayed. Note: When `outset-arrows` is `true`, the arrows are shown `"always"`.

-   `always`: Arrows are always displayed.
-   `auto`: Arrows are displayed when the carousel has most recently received interaction via mouse, and not displayed when the carousel has most recently received interaction via touch. On first load for touch devices, arrows are displayed until first interaction.
-   `never`: Arrows are never displayed.

###### `extraSpace`

Either `"around"` or undefined. This determines how extra space is allocated after displaying the calculated number of visible slides in the carousel. If `"around"`, white space is evenly distributed around the carousel with `justify-content: center`; otherwise, space is allocated to the right of the carousel for LTR documents and to the left for RTL documents.

###### `loop`

Either `true` or `false`, defaults to `true`. When true, the carousel will allow
the user to move from the first item back to the last item and visa versa. There
must be at least three slides present for looping to occur.

###### `outsetArrows`

Either `true` or `false`, defaults to `false`. When true, the carousel will display its arrows outset and on either side of the slides. Note that with outset arrows, the slide container will have an effective length of 100px less than the allotted space for its given container - 50px per arrow on either side. When false, the carousel will display its arrows inset and overlayed on top of the left and right edges of the slides.

###### `peek`

A number, defaults to `0`. This determines how much of an additional slide to show (on one or both sides of the current slide) as an affordance to the user indicating the carousel is swipeable.

##### Gallery slide visibility

###### `minVisibleCount`

A number, defaults to `1`. Determines the minimum number of slides that should be shown at a given time. Fractional values can be used to make part of a(n) additional slide(s)
visible.

###### `maxVisibleCount`

A number, defaults to [`Number.MAX_VALUE`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_VALUE). Determines the maximum number of slides that should be shown at a given time. Fractional values can be used to make part of a(n) additional slide(s) visible.

###### `minItemWidth`

A number, defaults to `1`. Determines the minimum width of each item, used to resolve how many whole items can be shown at once within the overall width of the gallery.

###### `maxItemWidth`

A number, defaults to [`Number.MAX_VALUE`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_VALUE). Determines the maximum width of each item, used to resolve how many whole items can be shown at once within the overall width of the gallery.

##### Slide snapping

###### `slideAlign`

Either `start` or `center`. When start aligning, the start of a slide (e.g. the
left edge, when horizontal aligning) is aligned with the start of a carousel.
When center aligning, the center of a slide is aligned with the center of a
carousel.

###### `snap`

Either `true` or `false`, defaults to `true`. Determines whether or not the
carousel should snap on slides when scrolling.
