---
title: Birth Rates across the US (1990 - 2009)
subtitle: A Data Visualization Project
author: Mythreyi S
framework: io2012
highlighter: highlight.js
mode: selfcontained

---

A picture is worth a thousand words
---
<style>
strong {
  font-weight: bold;
}
</style>
* CDC has published US birth rate data across all the states for the years 1990 - 2009. Below is a sample set of rows and columns from the data frame.


| Year| Alabama| Alaska| Arizona| Arkansas| California| Colorado| Connecticut|
|----:|-------:|------:|-------:|--------:|----------:|--------:|-----------:|
| 2009|    13.3|   16.2|    14.1|     13.8|       14.3|     13.7|        11.1|
| 2008|    13.8|   16.7|    15.3|     14.2|       15.0|     14.2|        11.5|
| 2007|    14.0|   16.2|    16.2|     14.6|       15.5|     14.6|        11.9|
| 2006|    13.7|   16.4|    16.6|     14.6|       15.4|     14.9|        11.9|

* It is very tedious to go through the individual states in the table to determine changes in birth rate in the US over the years.

* It is even more difficult to analyze the birth rate trend in all the states in a particular year.

* Just imagine going through the table (again!) to compare the birth rate changes in two or more states!

Here is a solution to the above issues - ***Interactive Data Visualization***.

---
NVD3 Chart
---
* Here is an NVD3 line chart from rCharts package with a sample set of data for 5 states. The user can determine the birth rate changes over the years in individual states and also select/deselect the legends to compare birth rates between two or more states.

<div id = 'chart' class = 'rChart nvd3'></div>
<script type='text/javascript'>
 $(document).ready(function(){
      drawchart()
    });
    function drawchart(){  
      var opts = {
 "dom": "chart",
"width":    800,
"height":    400,
"x": "Year",
"y": "Birth.Rate",
"group": "State",
"type": "lineChart",
"id": "chart" 
},
        data = [
 {
 "Year":           2009,
"State.Name": "Alaska",
"Birth.Rate":           16.2,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2008,
"State.Name": "Alaska",
"Birth.Rate":           16.7,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2007,
"State.Name": "Alaska",
"Birth.Rate":           16.2,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2006,
"State.Name": "Alaska",
"Birth.Rate":           16.4,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2005,
"State.Name": "Alaska",
"Birth.Rate":           15.8,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2004,
"State.Name": "Alaska",
"Birth.Rate":           15.8,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2003,
"State.Name": "Alaska",
"Birth.Rate":           15.5,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2002,
"State.Name": "Alaska",
"Birth.Rate":           15.4,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2001,
"State.Name": "Alaska",
"Birth.Rate":           15.8,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2000,
"State.Name": "Alaska",
"Birth.Rate":           15.9,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1999,
"State.Name": "Alaska",
"Birth.Rate":           15.9,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1998,
"State.Name": "Alaska",
"Birth.Rate":             16,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1997,
"State.Name": "Alaska",
"Birth.Rate":           16.2,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1996,
"State.Name": "Alaska",
"Birth.Rate":           16.5,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1995,
"State.Name": "Alaska",
"Birth.Rate":           16.9,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1994,
"State.Name": "Alaska",
"Birth.Rate":           17.7,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1993,
"State.Name": "Alaska",
"Birth.Rate":           18.5,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1992,
"State.Name": "Alaska",
"Birth.Rate":           19.9,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1991,
"State.Name": "Alaska",
"Birth.Rate":           20.5,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1990,
"State.Name": "Alaska",
"Birth.Rate":           21.6,
"State": "AK",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2009,
"State.Name": "Massachusetts",
"Birth.Rate":           11.4,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2008,
"State.Name": "Massachusetts",
"Birth.Rate":           11.9,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2007,
"State.Name": "Massachusetts",
"Birth.Rate":           12.1,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2006,
"State.Name": "Massachusetts",
"Birth.Rate":           12.1,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2005,
"State.Name": "Massachusetts",
"Birth.Rate":             12,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2004,
"State.Name": "Massachusetts",
"Birth.Rate":           12.2,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2003,
"State.Name": "Massachusetts",
"Birth.Rate":           12.5,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2002,
"State.Name": "Massachusetts",
"Birth.Rate":           12.5,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2001,
"State.Name": "Massachusetts",
"Birth.Rate":           12.7,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2000,
"State.Name": "Massachusetts",
"Birth.Rate":           12.9,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1999,
"State.Name": "Massachusetts",
"Birth.Rate":           12.8,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1998,
"State.Name": "Massachusetts",
"Birth.Rate":             13,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1997,
"State.Name": "Massachusetts",
"Birth.Rate":           12.9,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1996,
"State.Name": "Massachusetts",
"Birth.Rate":             13,
"State": "MA",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1995,
"State.Name": "Massachusetts",
"Birth.Rate":           13.3,
"State": "MA",
"fillKey": "(13.2,14]" 
},
{
 "Year":           1994,
"State.Name": "Massachusetts",
"Birth.Rate":           13.7,
"State": "MA",
"fillKey": "(13.2,14]" 
},
{
 "Year":           1993,
"State.Name": "Massachusetts",
"Birth.Rate":             14,
"State": "MA",
"fillKey": "(13.2,14]" 
},
{
 "Year":           1992,
"State.Name": "Massachusetts",
"Birth.Rate":           14.5,
"State": "MA",
"fillKey": "(14,15.1]" 
},
{
 "Year":           1991,
"State.Name": "Massachusetts",
"Birth.Rate":           14.7,
"State": "MA",
"fillKey": "(14,15.1]" 
},
{
 "Year":           1990,
"State.Name": "Massachusetts",
"Birth.Rate":           15.4,
"State": "MA",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2009,
"State.Name": "New York",
"Birth.Rate":           12.7,
"State": "NY",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2008,
"State.Name": "New York",
"Birth.Rate":           12.8,
"State": "NY",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2007,
"State.Name": "New York",
"Birth.Rate":           13.1,
"State": "NY",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2006,
"State.Name": "New York",
"Birth.Rate":             13,
"State": "NY",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2005,
"State.Name": "New York",
"Birth.Rate":           12.8,
"State": "NY",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2004,
"State.Name": "New York",
"Birth.Rate":             13,
"State": "NY",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2003,
"State.Name": "New York",
"Birth.Rate":           13.2,
"State": "NY",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2002,
"State.Name": "New York",
"Birth.Rate":           13.1,
"State": "NY",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2001,
"State.Name": "New York",
"Birth.Rate":           13.3,
"State": "NY",
"fillKey": "(13.2,14]" 
},
{
 "Year":           2000,
"State.Name": "New York",
"Birth.Rate":           13.6,
"State": "NY",
"fillKey": "(13.2,14]" 
},
{
 "Year":           1999,
"State.Name": "New York",
"Birth.Rate":           13.5,
"State": "NY",
"fillKey": "(13.2,14]" 
},
{
 "Year":           1998,
"State.Name": "New York",
"Birth.Rate":           13.8,
"State": "NY",
"fillKey": "(13.2,14]" 
},
{
 "Year":           1997,
"State.Name": "New York",
"Birth.Rate":           13.8,
"State": "NY",
"fillKey": "(13.2,14]" 
},
{
 "Year":           1996,
"State.Name": "New York",
"Birth.Rate":           14.2,
"State": "NY",
"fillKey": "(14,15.1]" 
},
{
 "Year":           1995,
"State.Name": "New York",
"Birth.Rate":           14.6,
"State": "NY",
"fillKey": "(14,15.1]" 
},
{
 "Year":           1994,
"State.Name": "New York",
"Birth.Rate":           15.1,
"State": "NY",
"fillKey": "(14,15.1]" 
},
{
 "Year":           1993,
"State.Name": "New York",
"Birth.Rate":           15.4,
"State": "NY",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1992,
"State.Name": "New York",
"Birth.Rate":           15.8,
"State": "NY",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1991,
"State.Name": "New York",
"Birth.Rate":           16.1,
"State": "NY",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1990,
"State.Name": "New York",
"Birth.Rate":           16.5,
"State": "NY",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2009,
"State.Name": "Utah",
"Birth.Rate":           19.4,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2008,
"State.Name": "Utah",
"Birth.Rate":           20.3,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2007,
"State.Name": "Utah",
"Birth.Rate":           20.8,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2006,
"State.Name": "Utah",
"Birth.Rate":             21,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2005,
"State.Name": "Utah",
"Birth.Rate":           20.9,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2004,
"State.Name": "Utah",
"Birth.Rate":           21.2,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2003,
"State.Name": "Utah",
"Birth.Rate":           21.2,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2002,
"State.Name": "Utah",
"Birth.Rate":           21.2,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2001,
"State.Name": "Utah",
"Birth.Rate":             21,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2000,
"State.Name": "Utah",
"Birth.Rate":           21.2,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1999,
"State.Name": "Utah",
"Birth.Rate":             21,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1998,
"State.Name": "Utah",
"Birth.Rate":           20.9,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1997,
"State.Name": "Utah",
"Birth.Rate":           20.3,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1996,
"State.Name": "Utah",
"Birth.Rate":           20.4,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1995,
"State.Name": "Utah",
"Birth.Rate":           19.6,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1994,
"State.Name": "Utah",
"Birth.Rate":           19.5,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1993,
"State.Name": "Utah",
"Birth.Rate":           19.6,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1992,
"State.Name": "Utah",
"Birth.Rate":           20.3,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1991,
"State.Name": "Utah",
"Birth.Rate":           20.2,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           1990,
"State.Name": "Utah",
"Birth.Rate":           21.1,
"State": "UT",
"fillKey": "(15.1,21.6]" 
},
{
 "Year":           2009,
"State.Name": "Vermont",
"Birth.Rate":            9.8,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2008,
"State.Name": "Vermont",
"Birth.Rate":           10.2,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2007,
"State.Name": "Vermont",
"Birth.Rate":           10.5,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2006,
"State.Name": "Vermont",
"Birth.Rate":           10.4,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2005,
"State.Name": "Vermont",
"Birth.Rate":           10.1,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2004,
"State.Name": "Vermont",
"Birth.Rate":           10.6,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2003,
"State.Name": "Vermont",
"Birth.Rate":           10.6,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2002,
"State.Name": "Vermont",
"Birth.Rate":           10.4,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2001,
"State.Name": "Vermont",
"Birth.Rate":           10.4,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           2000,
"State.Name": "Vermont",
"Birth.Rate":           10.7,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1999,
"State.Name": "Vermont",
"Birth.Rate":           10.9,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1998,
"State.Name": "Vermont",
"Birth.Rate":             11,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1997,
"State.Name": "Vermont",
"Birth.Rate":           11.1,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1996,
"State.Name": "Vermont",
"Birth.Rate":           11.4,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1995,
"State.Name": "Vermont",
"Birth.Rate":           11.5,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1994,
"State.Name": "Vermont",
"Birth.Rate":           12.6,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1993,
"State.Name": "Vermont",
"Birth.Rate":           12.9,
"State": "VT",
"fillKey": "(9.8,13.2]" 
},
{
 "Year":           1992,
"State.Name": "Vermont",
"Birth.Rate":           13.5,
"State": "VT",
"fillKey": "(13.2,14]" 
},
{
 "Year":           1991,
"State.Name": "Vermont",
"Birth.Rate":             14,
"State": "VT",
"fillKey": "(13.2,14]" 
},
{
 "Year":           1990,
"State.Name": "Vermont",
"Birth.Rate":           14.7,
"State": "VT",
"fillKey": "(14,15.1]" 
} 
]
  
      if(!(opts.type==="pieChart" || opts.type==="sparklinePlus" || opts.type==="bulletChart")) {
        var data = d3.nest()
          .key(function(d){
            //return opts.group === undefined ? 'main' : d[opts.group]
            //instead of main would think a better default is opts.x
            return opts.group === undefined ? opts.y : d[opts.group];
          })
          .entries(data);
      }
      
      if (opts.disabled != undefined){
        data.map(function(d, i){
          d.disabled = opts.disabled[i]
        })
      }
      
      nv.addGraph(function() {
        var chart = nv.models[opts.type]()
          .width(opts.width)
          .height(opts.height)
          
        if (opts.type != "bulletChart"){
          chart
            .x(function(d) { return d[opts.x] })
            .y(function(d) { return d[opts.y] })
        }
          
         
        
          
        chart.xAxis
  .axisLabel("Year")

        
        
        chart.yAxis
  .axisLabel("Birth Rate")
      
       d3.select("#" + opts.id)
        .append('svg')
        .datum(data)
        .transition().duration(500)
        .call(chart);

       nv.utils.windowResize(chart.update);
       return chart;
      });
    };
</script>

---
US Choropleth
---
<style type='text/css'>
img {
    max-height: 560px;
    max-width: 964px;
}
</style>
![width](choropleth.png)

---
The story behind
---
What's life without challenges?
===
* Creating the US choropleth had more than its fair share of challenges.
* It turned out that there are two versions of 'datamaps' library, one in rCharts and the other in rMaps package. 
* The 'datamaps' library in rCharts seems to be an older version. Using it to show the choropleth in the Shiny server not only masked the labels and legend but also somehow corrupted the nvd3 line chart.
* It took a lot of iterations to determine that the issue was with the 'datamaps' library version.
* The issue was resolved in Shiny by explicitly loading the 'datamaps' library from rMaps.
* To keep it simple in slidify, the choropleth is not displayed from an R code but as an image.

So, what's in the future?
===
* Resolve the 'datamaps' library issue and display the choropleth in Slidify using R code.
* Write a prediction algorithm to predict birth rates in future and include it in Shiny app.

