# jTableManager v 1.0
Inline editor for HTML tables compatible with Bootstrap.

## History
Based on the work of markcell
http://markcell.github.io/jquery-tabledit

And bluesatkv
https://bluesatkv.github.io/jquery-tabledit

## Basic usage

1. Add the jQuery tableManager plugin after jQuery library.

```
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>
<script src="jquery.tablemanager.min.js"></script>
```


2. Create Bootstrap table with data

```
<table class="table table-hover" id="my-table">
    <thead>
        <tr>
            <th>Id</th>
            <th>Column 1</th>
            <th>Column 2</th>
            <th>Column 3</th>
            <th>Column 4</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Example 1</td>
            <td>Example 2</td>
            <td>Example 3</td>
            <td>Example 4</td>
        </tr>
    </tbody>
</table>
```

3. Call the plugin on your existing table and specify the editable columns whatever you like.

```
$('#my-table').jTableManager({
    url: 'URL-TO-PHP-FILE',
    editButton: false,
    deleteButton: true,
    lang: 'en',
    restoreButton:false,
    disableSelectAutoFocus:true,
    cursorPosition:'end',
    hideDeletedRow: true,
    columns: {
        identifier: [1, 'id'],
        editable: [
          [2, 'name'], 
          [3, 'category', 'select', '{"0": "Cat 1", "1": "Cat 2", "2": "Cat 3", "3": "Cat 4"}'],
          [7, 'description', 'textarea'],
        ]
    },
    onDraw: function() {
        console.log('onDraw()');
    },
    onSuccess: function(data, textStatus, jqXHR) {
        console.log(data);
    },
    onFail: function(jqXHR, textStatus, errorThrown) {
    },
    onAlways: function() {
    },
    onAjax: function(action, serialize) {
    }
});
```

## New Features
https://github.com/eafarooqi/jTableManager/wiki

## Complete Documentation
Original example by _markcell_ you find on
http://markcell.github.io/jquery-tabledit/#documentation

Full complete documentation by BluesatKV on 
https://bluesatkv.github.io/jquery-tabledit/#documentation


## Changelog
See CHANGELOG.md on 
https://github.com/eafarooqi/jTableManager/blob/master/CHANGELOG.md

