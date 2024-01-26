Print a JSON object in the browser using JavaScript. Supports multi-level nested object/array.
```JavaScript
//Global Method to prettify JSON Object to display in browser.
const prettifyJson = {
	replacer: function(match, pIndent, pKey, pVal, pEnd){
		var key = '<span class=json-key>';
		var val = '<span class=json-value>';
		var str = '<span class=json-string>';
		var r = pIndent || '';
		if(pKey)
			r = r + key + pKey.replace(/[";]/g,'') + '</span>: ';
		if(pVal)
			r = r + (pVal[0] == '"'?str:val) + pVal + '<span>';
		return r + (pEnd || '');
	},
	render: funtion(jsonObj){
		var jsonLine = /^( *)("[\w]+": )?("[^"]*"|[\w.+-]*)?([,[{])?$/mg;
		return JSON.stringify(jsonObj, null, 4)
			.replace(/&/g, '&amp;').replace(/\\"/g,'&quot;')
			.replace(/</g, '&lt;').replace(/>/g, '&gt;')
			.replace(jsonLine, prettyJSON.replacer);
	}
}

//Displaying prettify JSON object in HTML
document.getElementById("jsonViewer").insertAdjacentHTML("afterend",
	prettifyJson.render(jsonObject)
)
```

```CSS
pre{
	background-color: #f8f8ff;
	border: 1px solid #c0c0c0;
	padding: 10px 20px;
	margin: 20px;
}
.json-key{ color: #a52a2a; }
.json-value{ color:#000080; }
.json-string{ color: #808000; }
```

```HTML
<pre>
	<code id="jsonViewer">
	</code>
</pre>
```

```JSON
{
	"id":"0001",
	"type":"donut",
	"name":"Cake",
	"image":{
		"url":"images/0001.jpg",
		"width":200,
		"height":200
	},
	"thumbnail":{
		"url":"images/thumbnails/0001.jpg",
		"width":32,
		"height":32
	}
}
```