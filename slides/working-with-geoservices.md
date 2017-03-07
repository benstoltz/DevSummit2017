<!-- .slide: data-background="img/esri-fed-summit-2017/bg-3.png" -->
## Working with Cedar

---

<!-- .slide: data-background="img/esri-fed-summit-2017/bg-6.png" -->
## Cedar Overview
<img src="https://docs.google.com/drawings/d/1pkPnCkNdg-3-t8H6f8xForlinz_GkCSCAQSps5Aki_k/pub?w=720&h=540" class="transparent" height="540" />

---

<!-- .slide: data-background="img/esri-fed-summit-2017/bg-6.png" -->
## Cedar example

```js
// create a new Cedar instance
var chart = new Cedar({
  "type":"bar" // shorthand for re-usable bar specification
});
```
<!-- .element: class="large" -->

---

<!-- .slide: data-background="img/esri-fed-summit-2017/bg-6.png" -->
## Cedar example

```js
// identify service to query data from
chart.datasets = [
    {
      "url":"https://server.arcgisonline.com/arcgis/rest/services/Demographis/USA_Population_Density/MapServer/4"
    }
];
```
<!-- .element: class="large" -->

Note:
smart defaults (`where: 1=1`)

---

<!-- .slide: data-background="img/esri-fed-summit-2017/bg-6.png" -->
## Cedar example

```js
// bind feature attributes to chart properties
chart.series = [
  {
    "category": {"field":"NAME","label":"US State"},
    "value": {"field":"TOTPOP_CY","label":"Population"}
  }
];
```
<!-- .element: class="large" -->

Note:
flattens feature `attributes` so you don't have to

---

<!-- .slide: data-background="img/esri-fed-summit-2017/bg-6.png" -->
## Cedar example

```js
// execute query and render chart at specified DOM element
chart.show({
  elementId: "#chart"
});
```
<!-- .element: class="large" -->

---

<!-- .slide: data-background="img/esri-fed-summit-2017/bg-6.png" -->
## Cedar example

<iframe width="100%" height="600" width="800" src="//jsfiddle.net/tomwayson/dox5o6w4/embedded/result,js,html/" allowfullscreen="allowfullscreen" frameborder="0"></iframe>

---

<!-- .slide: data-background="img/esri-fed-summit-2017/bg-4.png" -->
## Demo: Cedar charts
