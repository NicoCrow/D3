# D3 (Data-Driven Documents)

_library is written by Mike Bostock_

Link to library &lt;script src="http://d3js.org/d3.v3.min.js" charset="utf-8"&gt;&lt;/script&gt;

Select the &lt;svg&gt; element and select all of the &lt;circle&gt; elements (assuming they are on the DOM already) and modify their __cx__ attribute.
```javascript
d3.select('svg').selectAll('circle')
	.data([10, 20, 30, 40])
	.attr('cx', function(d){ return d; });
```

Append &lt;h1&gt; element to &lt;body&gt; [__.select()__]
```javascript
d3.select('body')
	.append('h1')
	.text('Hello, World!')
```

Select all __div__ elements with class __.foo__ (equivalent to _$('div.foo')_) [__.selecrAll()__]
```javascript
d3.selectAll('div.foo');
```

Change all of the divs to have a bg-color of green [__.style()__]
```javascript
d3.selectAll('div')
	.style('backgrount-color', 'green');
```

Divs with different bg-colors
```javascript
d3.selectAll('div')
	.style('backgrount-color', function(d, i){	//i - index of current element in the selector
		if(Math.random() > 0.5){
			return 'orange';
		} else {
			return 'green';
		}
	});
```

__.attr()__ method
```html
<body>
	<div>Hello</div>
	<div>World</div>
	<div>!</div>
</body>
```
```javascript
d3.selectAll('div')
	.attr('width', '100%');
```

