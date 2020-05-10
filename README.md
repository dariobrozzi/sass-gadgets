# SASS Gadgets

(Draft Version)

Just another SASS library, but based on W3C Standards and ITCSS concept. Having just the settings and tools(gadgets) layers for help you building your design system.

No attached to predefined ClassNames and overrides.
Feel free to apply gadgets into your components or create your own ClassNames selectors.
And all this, with a minimal CSS bundle at the end.

Happy coding!

## Getting Started

### Prerequisites
- A npm project for install this package.
- Last SASS package version for support module system features.

### Installing
Repository is on GitHub, so you need to add the entry to your npm config.
Other simple way is configure your root project file <code>.npmrc</code> like:

<code>
   
    registry=https://registry.npmjs.org
    
    @dariobrozzi:registry=https://npm.pkg.github.com
</code>

Then:
<code>npm install @dariobrozzi/sass-gadgets</code>

### How to use it

#### The Basis

Get all library and using a namespace

<pre>
<code>
@use '~@dariobrozzi/sass-gadgets/all' as gadgets;

// then use it
body {
    @include gadgets.fontStack(georgia);
}
</code>
</pre>

#### With Settings

Create a file '_gadgets.scss' at vendor or where you want. Do a forward from package.
Then at your main styles, use it passing the variables want to replace.

<pre><code>
// _gadgets.scss
@forward '~@dariobrozzi/sass-gadgets/all';

// styles.scss
@use 'gadgets' with (
    $entities: 'html, body, div, button, h1, h2, p, em, blockquote, code, pre',
);

// then use it
@include gadgets.resetDOM();
</code></pre>

### Using Fonts
<pre>
<code>
    // set font family
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


More info and examples comming next weeks.

## Authors

* **Dario Brozzi** - [GitHub](https://github.com/dariobrozzi)
