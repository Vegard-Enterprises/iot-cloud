#### Row style function

<div class="divider"></div>
<br/>

*function (rowData, ctx): {[key: string]: string}*

A JavaScript function used to compute timeseries row style depending on row value.

**Parameters:**

<ul>
  <li><b>rowData:</b> <code>TimeseriesRow</code> - A 
            TimeseriesRow object
            presenting <code>formattedTs</code> (a string value of formatted timestamp) and <br> timeseries values for each column declared in widget datasource configuration.
  </li>
  <li><b>ctx:</b> <code>WidgetContext</code> - A reference to WidgetContext that has all necessary API 
     and data used by widget instance.
  </li>
</ul>

**Returns:**

Should return key/value object presenting style attributes.

<div class="divider"></div>

##### Examples

* Set row background color depending on temperature value:

```javascript
var temperature = rowData.temperature;
var color = '#fff';
if (temperature) {
  if (temperature > 25) {
    color = 'red';
  } else {
    color = 'green';
  }
}
return {
  backgroundColor: color
};
{:copy-code}
```

<br>
<br>
