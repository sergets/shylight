# shylight
A simple and straightforward code to make an editable text input with basic syntax highlight by regexps

## Example

````js
shylight(
    document.getElementById('my-div'),
    {
        '\\d+' : 'number',                                     // Wrap numbers with '<span class="number">'
        '\\b([A-Z])([a-z]+)\\b' : function(_, first, second) { // Make initial uppercase Latin letters bold
            return '<b>' + first + '</b>' + second;
        }
    },
    function(val) {
        console.log('My div value changed to: ', val);
    }
);
````
