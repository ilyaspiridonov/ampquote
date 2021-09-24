# Bento Soundcloud

## Usage

The Bento Soundcloud component allows you to embed a Soundcloud clip. Use it as a web component [`<bento-soundcloud>`](#web-component), or a Preact/React functional component [`<BentoSoundcloud>`](#preact/react-Component).

### Web Component

You must include each Bento component's required CSS library to guarantee proper loading and before adding custom styles. Or use the light-weight pre-upgrade styles available inline. See [Layout and style](#layout-and-style).

The examples below demonstrate use of the `<bento-soundcloud>` web component.

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

The `bento-soundcloud` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children (slides) via a desired CSS layout (such as one defined with `height`, `width`, `aspect-ratio`, or other such properties):



#### Attributes

<table>
  <tr>
    <td width="40%"><strong>data-trackid</strong></td>
    <td>This attribute is required if <code>data-playlistid</code> is not defined.<br />
The value for this attribute is the ID of a track, an integer.</td>
  </tr>
  <tr>
    <td width="40%"><strong>data-playlistid</strong></td>
    <td>This attribute is required if <code>data-trackid</code> is not defined.
The value for this attribute is the ID of a playlist, an integer.</td>
  </tr>
  <tr>
    <td width="40%"><strong>data-secret-token (optional)</strong></td>
    <td>The secret token of the track, if it is private.</td>
  </tr>
  <tr>
    <td width="40%"><strong>data-visual (optional)</strong></td>
    <td>If set to <code>true</code>, displays full-width "Visual" mode; otherwise, it displays as "Classic" mode. The default value is <code>false</code>.</td>
  </tr>
  <tr>
    <td width="40%"><strong>data-color (optional)</strong></td>
    <td>This attribute is a custom color override for the "Classic" mode. The attribute is ignored in "Visual" mode. Specify a hexadecimal color value, without the leading # (e.g., <code>data-color="e540ff"</code>).</td>
  </tr>
</table>

### Preact/React Component

The examples below demonstrate use of the `<BentoSoundcloud>` as a functional component usable with the Preact or React libraries.

#### Example: Import via npm

[example preview="top-frame" playground="false"]

Install via npm:



[/example]

#### Layout and style

**Container type**

The `BentoSoundcloud` component has a defined layout size type. To ensure the component renders correctly, be sure to apply a size to the component and its immediate children (slides) via a desired CSS layout (such as one defined with `height`, `width`, `aspect-ratio`, or other such properties). These can be applied inline:



Or via `className`:



### Props

<table>
  <tr>
    <td width="40%"><strong>trackId</strong></td>
    <td>This attribute is required if <code>data-playlistid</code> is not defined.<br />
The value for this attribute is the ID of a track, an integer.</td>
  </tr>
  <tr>
    <td width="40%"><strong>playlistId</strong></td>
    <td>This attribute is required if <code>data-trackid</code> is not defined.
The value for this attribute is the ID of a playlist, an integer.</td>
  </tr>
  <tr>
    <td width="40%"><strong>secretToken (optional)</strong></td>
    <td>The secret token of the track, if it is private.</td>
  </tr>
  <tr>
    <td width="40%"><strong>visual (optional)</strong></td>
    <td>If set to <code>true</code>, displays full-width "Visual" mode; otherwise, it displays as "Classic" mode. The default value is <code>false</code>.</td>
  </tr>
  <tr>
    <td width="40%"><strong>color (optional)</strong></td>
    <td>This attribute is a custom color override for the "Classic" mode. The attribute is ignored in "Visual" mode. Specify a hexadecimal color value, without the leading # (e.g., <code>data-color="e540ff"</code>).</td>
  </tr>
</table>
