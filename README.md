# apollo-select
A spiced up Select Web Component with filtering, keyboard navigation and more, built with Polymer

Demo: http://peppe.github.io/apollo-select

## Using the component

### Basic usage

    <apollo-select id="my-select"></apollo-select>

id is of course optional but it helps you to configure it.

### Setting options
    var mySelect = document.querySelector('#my-select');
    mySelect.values = [
      "Chinchilla",
      "Pegasus",
      "Firefly",
    ];
    
### Selecting an option
Do this after you have added that option to the list with mySelect.values 
    mySelect.value="Pegasus";

### Setting a placeholder text into the input
    mySelect.placeholder = "What is your favorite animal?";
    
### Getting an event when the user selects a value
    mySelect.addEventListener('value-changed', function(e) {
      document.querySelector('.valuefield').innerHTML='Value: ' + e.detail.value;
    });

## Possible todo's`
Nothing decided, just listing a few possibilites. Not directly sure in which direction I should take this.

 - an addItem('string') function
 - Light DOM version for configuring. I tried to this when Polymer 0.5 was still the hot stuff, but failed. Some parts have been rewritten since and I should revisit this.
 - A dropdown with columns in it (with vaadin-grid)
 - Switch custom dropdown to Polymer's iron-dropdown?
 - Switch custom overlay to Polymer's iron-overlay-behavior?
