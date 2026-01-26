#### Cell content function

<div class="divider"></div>
<br/>

*function (value, rowData, ctx): string*

A JavaScript function used to compute timeseries cell content HTML depending on timeseries field value.

**Parameters:**

<ul>
  <li><b>value:</b> <code>any</code> - An entity field value displayed in the cell.
  </li>
  <li><b>rowData:</b> <code>TimeseriesRow</code> - A 
            TimeseriesRow object
            presenting <code>formattedTs</code> (a string value of formatted timestamp) and <br> timeseries values for each column declared in widget datasource configuration.
  </li>
  <li><b>ctx:</b> <code>WidgetContext</code> - A reference to WidgetContext that has all necessary API 
     and data used by widget instance.
  </li>
</ul>

**Returns:**

Should return string value presenting cell content HTML.

<div class="divider"></div>

##### Examples

* Styled cell content for temperature field:

```javascript
var temperature = value;
var color = '#fff';
if (temperature) {
  if (temperature > 25) {
    color = 'red';
  } else {
    color = 'green';
  }
}
return '<div style="border: 2px solid #0072ff; ' +
  'border-radius: 10px; padding: 5px; ' +
  'color: #fff; ' +
  'background-color: '+ color +'; ' +
  'text-align: center;">' + temperature + '</div>';
{:copy-code}
```

<br>
<br>
