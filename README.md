# SASS Gadgets

(Draft Version)

Just another SASS library. Based on W3C Standards and ITCSS concept file structure. 
Having just the settings and tools(gadgets) layers for help you building your design system.

No attached to predefined ClassNames and overrides.
Feel free to apply gadgets into your components or create your own ClassNames selectors.
And all this, with a minimal CSS bundle at the end.

Happy coding!

## Getting Started

### Prerequisites
- A npm project for install this package.
- Last SASS package version for support module system features.

### Installing

<code>
   npm i sass-gadgets
</code>

### How to use it

#### The Basis

Get all library and using a namespace

<pre>
<code>
@use '~sass-gadgets/all' as gadgets;

// then use it
body {
    @include gadgets.fontStack(georgia);
}
</code>
</pre>

#### With Settings

Create a file '_gadgets.scss' at vendor or where you want. Do a forward from package.
Then at your main styles, use it passing the variables want to replace.

<pre><code>// _gadgets.scss

@forward '~sass-gadgets/all';
</code></pre>

<pre><code>// styles.scss

@use 'gadgets' with (
    $entities: 'html, body, div, button, h1, h2, p, em, blockquote, code, pre',
);

@include gadgets.resetDOM();
</code></pre>

### Using Fonts
<pre>
<code>// set font family
@include gadgets.fontStack(arialnarrow);
    
// set all properties defined on sets
@include gadgets.fontSet(large);
    
// set just font size defined on sets
@include gadgets.fontSize(normal);
</code>
</pre>


### Using FontAwesome Icons

<pre><code>
$your-assets-path: 'assets/fonts';

@include gadgets.initializeFontAwesome($your-assets-path);

a.linkedin:before {
    @include gadgets.iconFontAwesome(linkedin, brands);
}
</code></pre>


## Authors

* **Dario Brozzi** - [GitHub](https://github.com/dariobrozzi)
