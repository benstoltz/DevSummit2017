## Objective
Inform developers/decision that we are actively developing Cedar as a tool to help them make effective visualizations of geoservices and to have them try Cedar in their projects.

## What makes an effective visualization?

TODO

## How Cedar helps you make effective visualizations

### Working with geoservice data
  - default query parameters (`where: 1=1`)
  - mapping feature attributes to chart parameters
  - works with or with out map

### Intelligent defaults
 - TODO

## Where we're headed

### Using Cedar in Open Data (2016)
- Open Data and Hub requirements actively driving Cedar development
 - better support and examples of SQL expressions in queries
 - ability to transform data returned from server
- More production ready, added:
 - query callback for error handling
 - timeouts for slow loading Data
 - addon for Ember apps [ember-cli-cedar]

DEMO: Cedar in Open Data

- "Dogfooding" better understanding of areas we can improve:
  - Better support for multi-series charts
  - More chart types
  - Better default styling for charts

### Support for multi-series charts
- (potentially breaking) change to Cedar's JSON format (v1.0)
- adding deprecations to ease transition for existing charts (^0.9)

### Switching chart library from vega to amCharts?
- Basing cedar on [amCharts] would make it easier to
 - create and customize new chart types
 - customize or extend existing built-in chart types
 - style and theme charts

DEMO: Cedar amCharts

 - still exploring and welcome your input

## Conclusion
We're using Cedar to make the visualizations you see in Open Data and that has been driving improvements in Cedar, and we're very excited about the improvements we're planning for 2017. The next time you need to visualize geoservice data in a JavaScript application, we encourage you to try Cedar.

## Resources
2016 DevSummit Cedar Talk
 - [slides](https://github.com/ajturner/presentations/tree/gh-pages/geodev-2016-cedar)

[ember-cli-cedar]:https://github.com/ArcGIS/ember-cli-cedar
 - [demo](https://arcgis.github.io/ember-cli-cedar/)

[amCharts]:https://www.amcharts.com/javascript-charts/
