# AI Taxonomies

### AI Capabilities


```javascript
d3.select('button#export').on('click', function() {
  var config = {
    filename: 'customFileName',
  }
  d3_save_svg.save(d3.select('svg').node(), config);
});
```


### AI Design Patterns



#### embedRasterImages(svgElement)
A convenience function for converting all referenced raster images in an SVG element to base64 data via data URI, so that it is embedded in the SVG. This ensures that the downloaded image will contain the raster image. Probably should be updated to just directly convert a referenced link to data URI instead of doing it in two separate steps.

```javascript
svg
  .append('g')
   .append('image')
      .attr('xlink:href', 'assets/test.png')
      .attr("width", 100)
      .attr("height", 100)
      .attr("x", (width / 2)  - 50)
      .attr("y", (height / 6) * 5);

d3_save_svg.embedRasterImages(svg.node());
 ```

### Contributing
`npm install` to get the development dependencies, test and build.

Testing is via [Tape](https://github.com/substack/tape) and [jsdom](https://github.com/tmpvar/jsdom). Right now the tests are pretty rudimentary. Also `index.html` serves as a good check on whether things are working.

Development is done using the [git-flow](http://nvie.com/posts/a-successful-git-branching-model/) workflow. Please merge changes into the `develop` branch.

See [CONTRIBUTING.md](/CONTRIBUTING.md) for additional information.
