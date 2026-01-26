#### Node text function

<div class="divider"></div>
<br/>

*function (nodeCtx): string*

A JavaScript function used to compute text or HTML code for the current node.

**Parameters:**

<ul>
  <li><b>widgetCtx:</b> <code>WidgetContext</code> - A reference to WidgetContext that has all necessary API 
     and data used by widget instance.
  </li>
  <li><b>nodeCtx:</b> <code>HierarchyNodeContext</code> - An 
            HierarchyNodeContext object
            containing <code>entity</code> field holding basic entity properties <br> (ex. <code>id</code>, <code>name</code>, <code>label</code>) and <code>data</code> field holding other entity attributes/timeseries declared in widget datasource configuration.
   </li>
</ul>

**Returns:**

Should return string value presenting text or HTML for the current node.

<div class="divider"></div>

##### Examples

* Display entity name and optionally temperature value if it is present in entity attributes/timeseries:

```javascript
var data =  nodeCtx.data;
var entity = nodeCtx.entity;
var text = entity.name;
if (data.hasOwnProperty('temperature') && data['temperature'] !== null) {
  text += " <b>"+ data['temperature'] +" °C</b>";
}
return text;
{:copy-code}
```

<br>
<br>
