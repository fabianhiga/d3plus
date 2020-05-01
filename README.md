<!doctype html>
<meta charset="utf-8">

<script src="//d3plus.org/js/d3.js"></script>
<script src="//d3plus.org/js/d3plus.js"></script>

<div id="vizStacked"></div>

<div id="vizPie"></div>

<script>
  var url =
      "https://raw.githubusercontent.com/fabianhiga/d3plus/master/data.tsv";
  d3plus.viz()
    .container("#vizStacked")
    .data(url)
  //  .type("pie")
    .type("stacked")
    .x("año")
    .format("es_Es")
    .id("titulo")
 //.size("cant")
    .y("cant")
    .time("año")
    .shape({"interpolate":"monotone"})
  /*basis, basis-open, cardinal, monotone, cardinal-open, step, step-before, step-after*/
    .draw()
</script>

<script>
  var url =
"https://raw.githubusercontent.com/fabianhiga/d3plus/master/data.tsv";
  d3plus.viz()
    .container("#vizPie")
    .data(url)
    .type("pie")
    .format("es_Es")
    .id("titulo")
    .size("cant")
    .time("año")
    .draw()
</script>
