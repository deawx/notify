# Checkify
A light-weight, mobile-ready and customizable form validation plugin for jQuery, inspired by [Validetta](https://github.com/hsnaydd/validetta)

## Usage

Include `checkify.js` and `checkify.css` to your page

```
<link rel="stylesheet" href="checkify.css" />

<!-- checkify is depends on jQuery -->
<script src="jquery.js"></script>
<script src="checkify.js"></script>
```

__HTML__

```html
<!-- can be any html element, refer to container option -->
<form id="my-form">            
    <input type="text" data-checkify="minlen=10,required,number" />            
    <button>click me</button>
</form>
```

__JS__

```js
$('#my-form').checkify({
    // options
    onError: function () {
    	console.log('error');
    },
    onValid: function () {
    	console.log('valid');
    }
});
```

## Available options

```js
message: {    
    inactive: false,
    // if true. error message won't be shown for required cases
    inactiveForRequired: true,
    // horizontal gap for error message box
    hGap: null,
    // vertical gap for error message box
    vGap: null,
    // can be right or left
    position: 'left',
    required: 'This field is required.',
    email: 'Invalid data.',
    regex: 'Invalid data.',
    number: 'Invalid data, only numbers allowed.',
    maxlen: 'Maximum {count} characters allowed.',
    minlen: 'Minimum {count} characters allowed.',
    maxChecked: 'Maximum {count} options allowed.',
    minChecked: 'Please select at least {count} options.',
    maxSelected: 'Maximum {count} selection allowed.',
    minSelected: 'Minimum {count} selection allowed.',
    notEqual: 'Fields do not match.',
    different: 'Fields cannot be the same as each other'
},
realTime: false,
// css selector or jQuery object, checkify will search for elements inside this
container: null,
// css selector, this will be used as trigger checkify
trigger: null,
// callback, can be function  
onValid: null,
// callback, can be function
onError: null
```

## License

[MIT](https://github.com/dehghani-mehdi/checkify/blob/master/LICENSE)
