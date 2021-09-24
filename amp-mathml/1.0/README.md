# Bento MathML

## Usage

Renders a MathML formula in an iframe.

### Web Component

You must include each Bento component's required CSS library to guarantee proper loading and before adding custom styles. Or use the light-weight pre-upgrade styles available inline. See [Layout and style](#layout-and-style).

The examples below demonstrate use of the `<bento-mathml>` web component.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:



[/example]

#### Example: Include via `<script>`

The example below contains an `bento-mathml` with three sections. The
`expanded` attribute on the third section expands it on page load.

[example preview="top-frame" playground="false"]



[/example]

#### Layout and style

Each Bento component has a small CSS library you must include to guarantee proper loading without [content shifts](https://web.dev/cls/). Because of order-based specificity, you must manually ensure that stylesheets are included before any custom styles.



Alternatively, you may also make the light-weight pre-upgrade styles available inline:



#### Attributes

##### `data-formula` (required)

Specifies the formula to render.

##### `inline` (optional)

If specified, the component renders inline (`inline-block` in CSS).

##### `title` (optional)

Define a `title` attribute for the component to propagate to the underlying `<iframe>` element. The default value is `"MathML formula"`.

#### Styling

You may use the `bento-mathml` element selector to style the accordion freely.

### Preact/React Component

The examples below demonstrates use of the `<BentoMathml>` as a functional component usable with the Preact or React libraries.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:



[/example]

#### Layout and style

**Container type**

The `BentoMathml` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children via a desired CSS layout (such as one defined with `height`, `width`, `aspect-ratio`, or other such properties). These can be applied inline:



#### Props

##### `formula` (required)

Specifies the formula to render.

##### `inline` (optional)

If specified, the component renders inline (`inline-block` in CSS).

##### `title` (optional)

Define a `title` attribute for the component to propagate to the underlying `<iframe>` element. The default value is `"MathML formula"`.
