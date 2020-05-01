# SASS Gadgets
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
<code>
    @use '~@dariobrozzi/sass-gadgets/index' as gadgets;
    
    @include g.resetDOM();
    
    body {
      @include g.fontStack(arial);
    
      background: g.$color-black;
      color: g.$color-white;
    }
    
    h1, h2, h3, h4, h5, h6 {
      @include g.fontStack(georgia);
    }
    
    button {
      @include g.button();
    }

</code>

- Just import what you need. Variables, tools, or both.
- Rewrite variables so you can setup your fonts, colors, paddings and so on.
- Call mixins into your components or ClassNames selectos.

More info and examples comming next weeks.

## Authors

* **Dario Brozzi** - [GitHub](https://github.com/dariobrozzi)
