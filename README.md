# netart-helpers

#### Helper functions to programmatically create an Element, apply classes, ID, attributes and Styles through one function call. 

The helpers.js file contains four functions 

**applyStyle(el, property, value, unit)**
> *This function is used to apply a single style to an HTML element, the syntax to apply the style would be* 
```
   applyStyle(document.getElementById('rect'), 'left', 20, 'px'); 
```
> *Unit is an optional parameter as some styles dont need unit -> example => background: rgba(100,100,100,100)* 

**applyStyleObj(el, styleObjArr)**
> *This function is used to apply a multiple styles to an HTML element, the syntax to apply the style would be* 
```
    applyStyleObj(rect, [
        {property: 'left', value: event.clientX, unit: 'px'},
        {property: 'top', value: event.clientY, unit: 'px'}
    ]); 
```
> *This function takes in an object array of styles with property, value and unit. Unit is optional as some styles dont need it -> example => color: blue* 

**appendElement(parent_element, element_type, classList, ID, attributeArr)**
> *This function is used to create and append an element to the DOM* 
```
   // class array, ID and attribute array are all optional
        appendElement(body, 'div'); 
   // following is with class array
        appendElement(body, 'div', ["rect"]); 
   // following is with id 
        appendElement(body, 'div', ["rect"], "rect"); 
   // for attribute array, attribute array is array of objects {type: 'custom_attribute', value: 'custom_value'}
```
> *All class Array, ID and attribute array are optional*

**randomInt(min, max)**
> *This function is used to generate a random integer in the given range* 
```
   randomInt(4,10);
```
