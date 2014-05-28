## About:

jquery-handsontable-csv is an utility to export handsontable as csv files.
It includes functions to: 

* Generate a string for later processing
* Trigger a download of the generated csv file

## Example:

Make sure you include the js file right after handsontable.js and before handsontable.css, example:

``` html
...

<script src="include/javascript/jquery.handsontable.full.js"></script>
<script src="include/javascript/jquery.handsontable.csv.js"></script>
<link rel="stylesheet" media="screen" href="include/javascript/jquery.handsontable.full.css">

...
```

On js create a handsontable with some data (visit the [handsontable docs](https://github.com/warpech/jquery-handsontable/wiki/Options#constructor-options) for more info):

``` js
$("#table").handsontable({
    ...
});

var instance = $("#table").handsontable('getInstance');

instance.loadData( ... );
```

You can now generate the csv file as string:

``` js
var csv_string = handsontable2csv.string(instace);
```

Or trigger a download:

``` js
handsontable2csv.download(instance, "filename.csv");
```
