## About:

jquery-handsontable-csv is an utility to export handsontable as csv files.
It includes functions to: 

* Generate a string for later processing
* Trigger a download of the generated csv file (use [FileSaver.js](https://github.com/eligrey/FileSaver.js/) for a browser compatible solution)

## Example:

Include the js file right after handsontable.js and before handsontable.css, example:

``` html
...

<script src="js/jquery.handsontable.full.js"></script>
<script src="js/jquery.handsontable.csv.js"></script>
<link rel="stylesheet" media="screen" href="css/jquery.handsontable.full.css">

...
```

On js create a handsontable with some data (visit the [handsontable docs](https://github.com/warpech/jquery-handsontable/wiki/Options#constructor-options) for more info):

``` javascript
$("#table").handsontable({
    ...
});
var instance = $("#table").handsontable('getInstance');
instance.loadData( ... );
```

You can now generate the csv file as string:

``` javascript
var csv_string = handsontable2csv.string(instance);
```

Or trigger a download:

``` javascript
handsontable2csv.download(instance, "filename.csv");
```
