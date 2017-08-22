# Delay Keyup

**Sets an event handler when a keyup event fires after a specified timeout.**

## Install

```sh
npm install delay-keyup
```

# Example

```html
<input type="text" name="test"/>

<script src="jquery.js"></script>
<script src="delay-keyup.js"></script>
<sciprt>
    //There are several ways to use this plugin:
    //First, HTMLElement
    document.querySelector("input").delayKeyup(function(){
        this.value = this.value.toUpperCase();
    });

    //Second, NodeList
    document.querySelectorAll("input").delayKeyup(function(){
        this.value = this.value.toUpperCase();
    });

    //Third, jQuery
    $("input").daleyKeyup(function(){
        $(this).val( $(this).val().toUpperCase() );
    });

    //Or, just call the function
    delayKeyup("input", function(){
        this.value = this.value.toUpperCase();
    });
</sciprt>
```

Import in WebPack

```javascript
import delayKeyup from "delay-keyup";
//Or
import "delay-keyup"; //Recommanded
```

Or in AMD

```javascript
define(["delay-timeout"], function(){
    //Do stuffs here...
});
```

## Sets a specified timeout

Default, the event handler will be triggered after 1500 milliseconds, but you 
can pass the second or third argument to this function a number to specified
a custom timeout.

```javascript
import "delay-keyup";

//The second argument
document.querySelector("input").delayKeyup(function(){
    this.value = this.value.toUpperCase();
}, 3000);

//The third argument
delayKeyup("input", function(){
    this.value = this.value.toUpperCase();
}, 3000);
```