# D3 (Data-Driven Documents)
_library is written by Mike Bostock_

Select the &lt;svg&gt; element and select all of the &lt;circle&gt; elements (assuming they are on the DOM already) and modify their __cx__ attribute.
```javascript
d3.select('svg').selectAll('circle')
	.data([10, 20, 30, 40])
	.attr('cx', function(d){ return d; });
```