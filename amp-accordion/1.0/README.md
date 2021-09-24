# Bento Accordion

## Usage

The Bento Accordion component allows you to display collapsible and expandable
content sections. This component provides a way for viewers to glance at the
content outline and jump to any section. Effective use reduces scrolling needs
on mobile devices.

Use Bento Accordion as a web component ([`<bento-accordion>`](#web-component)), or a Preact/React functional component ([`<BentoAccordion>`](#preact/react-component)).

-   A Bento Accordion accepts one or more `<section>` elements as its direct
    children.
-   Each `<section>` must contain exactly two direct children.
-   The first child in a `<section>` is the heading for that section of the
    Bento Accordion. It must be a heading element such as `<h1>-<h6>` or
    `<header>`.
-   The second child in a `<section>` is the expandable/collapsible content.
    -   It can be any tag allowed in [AMP HTML](https://github.com/ampproject/amphtml/blob/main/docs/spec/amp-html-format.md).
-   A click or tap on a `<section>` heading expands or collapses the section.
-   A Bento Accordion with a defined `id` preserves the collapsed or expanded
    state of each section while the user remains on your domain.

### Web Component

You must include each Bento component's required CSS library to guarantee proper loading and before adding custom styles. Or use the light-weight pre-upgrade styles available inline. See [Layout and style](#layout-and-style).

The examples below demonstrate use of the `<bento-accordion>` web component.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:


[/example]

#### Example: Include via `<script>`

The example below contains an `bento-accordion` with three sections. The
`expanded` attribute on the third section expands it on page load.

[example preview="top-frame" playground="false"]


[/example]

#### Interactivity and API usage

Bento enabled components in standalone use are highly interactive through their API. The `bento-accordion` component API is accessible by including the following script tag in your document:



##### Actions

**toggle()**
The `toggle` action switches the `expanded` and `collapsed` states of
`bento-accordion` sections. When called with no arguments, it toggles all sections
of the accordion. To specify a specific section, add the `section` argument and
use its corresponding `id` as the value.



**expand()**
The `expand` action expands the sections of the `bento-accordion`. If a section
is already expanded, it stays expanded. When called with no arguments, it
expands all sections of the accordion. To specify a section, add the `section` argument, and use its corresponding `id` as the value.



**collapse()**
The `collapse` action collapses the sections of the `bento-accordion`. If a
section is already collapsed, it stays collapsed. When called with no arguments,
it collapses all sections of the accordion. To specify a section, add the
`section` argument, and use its corresponding `id` as the value.



##### Events

The `bento-accordion` API allows you to register and respond to the following events:

**expand**
This event is triggered when an accordion section is expanded and is dispatched from the expanded section.

See below for example.

**collapse**
This event is triggered when an accordion section is collapsed and is dispatched from the collapsed section.

In the example below, `section 1` listens for the `expand` event and expands `section 2` when it is expanded. `section 2` listens for the `collapse` event and collapses `section 1` when it is collapsed.

See below for example.



#### Layout and style

Each Bento component has a small CSS library you must include to guarantee proper loading without [content shifts](https://web.dev/cls/). Because of order-based specificity, you must manually ensure that stylesheets are included before any custom styles.


Alternatively, you may also make the light-weight pre-upgrade styles available inline:



#### Attributes

##### animate

Include the `animate` attribute in `<bento-accordion>` to add a "roll down"
animation when the content is expanded and "roll up" animation when collapsed.

This attribute can be configured to based on a [media query](./../../../docs/spec/amp-html-responsive-attributes.md).

[example preview="top-frame" playground="true" imports="bento-accordion:1.0"]



[/example]

##### expanded

Apply the `expanded` attribute to a nested `<section>` to expand that section when the page loads.

[example preview="top-frame" playground="true" imports="bento-accordion:1.0"]



[/example]

##### expand-single-section

Allow only one section to expand at a time by applying the `expand-single-section` attribute to the `<bento-accordion>` element. This means if a user taps on a collapsed `<section>`, it will expand and collapse other expanded `<section>`'s.

[example preview="top-frame" playground="true" imports="bento-accordion:1.0"]



[/example]

#### Styling

You may use the `bento-accordion` element selector to style the accordion
freely.

Keep the following points in mind when you style an amp-accordion:

-   `bento-accordion` elements are always `display: block`.
-   `float` cannot style a `<section>`, heading, nor content elements.
-   An expanded section applies the `expanded` attribute to the `<section>`
    element.
-   The content element is clear-fixed with `overflow: hidden` and hence cannot
    have scrollbars.
-   Margins of the `<bento-accordion>`, `<section>`, heading, and content elements
    are set to `0`, but can be overridden in custom styles.
-   Both the header and content elements are `position: relative`.

### Preact/React Component

The examples below demonstrates use of the `<BentoAccordion>` as a functional component usable with the Preact or React libraries.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:




[/example]

#### Interactivity and API usage

Bento components are highly interactive through their API. The `BentoAccordion` component API is accessible by passing a `ref`:


##### Actions

The `BentoAccordion` API allows you to perform the following actions:

**toggle()**
The `toggle` action switches the `expanded` and `collapsed` states of
`bento-accordion` sections. When called with no arguments, it toggles all sections
of the accordion. To specify a specific section, add the `section` argument and
use its corresponding `id` as the value.



**expand()**
The `expand` action expands the sections of the `bento-accordion`. If a section
is already expanded, it stays expanded. When called with no arguments, it
expands all sections of the accordion. To specify a section, add the `section` argument, and use its corresponding `id` as the value.


**collapse()**
The `collapse` action collapses the sections of the `bento-accordion`. If a
section is already collapsed, it stays collapsed. When called with no arguments,
it collapses all sections of the accordion. To specify a section, add the
`section` argument, and use its corresponding `id` as the value.



##### Events

The Bento Accordion API allows you to respond to the following events:

**onExpandStateChange**

This event is triggered on a section when an accordion section is expanded or collpased and is dispatched from the expanded section.

See below for example.

**onCollapse**

This event is triggered on a section when an accordion section is collapsed and is dispatched from the collapsed section.

In the example below, `section 1` listens for the `expand` event and expands `section 2` when it is expanded. `section 2` listens for the `collapse` event and collapses `section 1` when it is collapsed.

See below for example.



#### Layout and style

**Container type**

The `BentoAccordion` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children via a desired CSS layout (such as one defined with `height`, `width`, `aspect-ratio`, or other such properties). These can be applied inline:



#### Props

##### BentoAccordion

###### animate

If true, then uses "roll-down" / "roll-up" animation during the expansion and collapse of each section
Default: `false`

###### expandSingleSection

If true, then expanding 1 section will automatically collapse all other sections:
Default: `false`

##### BentoAccordionSection

###### animate

If true, then uses "roll-down" / "roll-up" animation during the expansion and collapse the section
Default: `false`

###### expanded

If true, expands the section.
Default: `false`

###### onExpandStateChange



Callback to listen for expand state changes. Takes a boolean flag as parameter indicating whether the section was just expanded (`false` indicates it was collapsed)

##### BentoAccordionHeader

##### Common props

This component supports the [common props](../../../docs/spec/bento-common-props.md) for React and Preact components.

BentoAccordionHeader does not yet support any custom props

##### BentoAccordionContent

##### Common props

This component supports the [common props](../../../docs/spec/bento-common-props.md) for React and Preact components.

BentoAccordionContent does not yet support any custom props
