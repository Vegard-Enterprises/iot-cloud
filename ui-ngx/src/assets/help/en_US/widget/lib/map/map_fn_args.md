  <li><b>data:</b> <code>FormattedData</code> object associated with data layer (markers/polygons/circles) or data point of the route (trips data layer).<br/>
     Represents basic entity properties (ex. <code>entityId</code>, <code>entityName</code>)<br/>and provides access to other entity attributes/timeseries declared in datasource of the data layer configuration.
  </li>
  <li><b>dsData:</b> <code>FormattedData[]</code> - All available data associated with data layers including additional datasources as array of FormattedData objects<br/>
     resolved from configured datasources. Each object represents basic entity properties (ex. <code>entityId</code>, <code>entityName</code>)<br/>
     and provides access to other entity attributes/timeseries declared in datasources of data layers configuration including additional datasources of the map configuration.
  </li>
  <li><b>ctx:</b> <code>WidgetContext</code> - A reference to WidgetContext that has all necessary API 
     and data used by widget instance.
  </li>
