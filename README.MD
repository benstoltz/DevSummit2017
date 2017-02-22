## Objective
Inform developers/decision that we are actively developing Cedar as a tool to help them make effective visualizations of geoservices and to have them try Cedar in their projects.

## Intro

### What is a visualization

Visualizations are any medium to present data, visually, to a visual consumer.

### Visualizations (Carto and beyond!)
  - Cartography
  - Charts
  - Infographics
  - Tables

### Brief History of Visualizations (Time?)
  - Cholera map
  - etc

## What makes an effective visualization?

### Why do we visualize data?
  - Cognitive understanding is faster when visually consumed
  - To understand the data
  - To frame the data in a different perspective thereby making it easier to reason and consume

### Methods to understand the data
  - Compare
  - Sort
  - Filter
  - Highlight
  - Aggregate
  - Re Express


## How Cedar helps you make effective visualizations

### Philosophy
- state of the art vizualizations
- re-usable, sharable
- integrated w/ ArcGIS API
- overridable, but smart defaults (from query params to chart types and styles)

### Cedar Overview (graphic)
Spec + Data + Mappings => Cedar => Chart

### Working with Cedar
1. (work through https://esri.github.io/cedar/tutorial/) and note:
 - default query parameters (`where: 1=1`)
 - flattens feature `attributes` so you don't have to

DEMO:
1. load https://esri.github.io/cedar/examples/map-to-chart-interaction.html
 - 2 ways to work w/ map Cedar does own summary query, or
1. load https://esri.github.io/cedar/examples/inlined-data.html
 - get data from a feature layer directly and add to chart
3. Briefly load scatter, pie, bubble, grouped bar, horizontal bar to demonstrate the other chart types

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
1. http://opendata.arcgis.com/ and search for "bikes" near Washington D.C.
1. Choose first result "DC Bike Accidents 2013" http://opendata.arcgis.com/datasets/dcdev::dc-bike-accidents-2013
1. Goal: give user idea of distribution of data so they can decide if it's useful to them
1. Explain Chart/Map Visualization icons
1. Click on "Day", chart clearly shows less on Sun, but from map hard to tell
1. Click on "Quadrant", map pretty much shows most are in NW, but it's very clear from chart
1. Click on "Time"
 - chart clearly shows seasonal trend, not visible in map
 - explain "smart" binning of continuous values (data range = year, so bin by month)
1. back to results list and click on "DC Bike Lanes" http://opendata.arcgis.com/datasets/Story::dc-bike-lanes
1. Click on "YEAR_INSTALLED"
 - explain equal interval binning of continuous numeric data
NOTE:
 - would be good to show another dataset w/ shorter/longer span to show binning by years/days

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
1. Got to bar https://esridc.github.io/cedar-amcharts/bar.html
 - same visualization as as existing cedar
1. show action drop down, download as PNG
 - but w/ extra user features
1. Go to timeline https://esridc.github.io/cedar-amcharts/timeline.html and show zoom in/out
 - chart types that we've struggled to make good default visualizations w/ vega are better in AmCharts
1. Go to pie https://esridc.github.io/cedar-amcharts/pie.html
 - better labels, colors, legend
1. Go to Timeclock https://esridc.github.io/cedar-amcharts/radar.html
 - easier for us to provide new chart types
1. Go to line https://esridc.github.io/cedar-amcharts/line.html
 - and have them support multi-series charts (query 2 columns, mapped to 2 series)
1. Go to DC Collision Injuries: https://esridc.github.io/cedar-amcharts/injuries.html
 - stacked or grouped bar charts

- still exploring and welcome your input

## Conclusion
We're using Cedar to make the visualizations you see in Open Data and that has been driving improvements in Cedar, and we're very excited about the improvements we're planning for 2017. The next time you need to visualize geoservice data in a JavaScript application, we encourage you to try Cedar.

## Resources
2016 DevSummit Cedar Talk
 - [slides](https://github.com/ajturner/presentations/tree/gh-pages/geodev-2016-cedar)

[ember-cli-cedar]:https://github.com/ArcGIS/ember-cli-cedar
 - [demo](https://arcgis.github.io/ember-cli-cedar/)

[amCharts]:https://www.amcharts.com/javascript-charts/

## Removed Sections

### Working with geoservice data
- primary value add: binding feature attributes to chart parameters
- [geoservices api](http://geoservices.github.io/)
  - query
  - spatial filtering
  - statistics
  - aggregations
  - limited SQL expression support
