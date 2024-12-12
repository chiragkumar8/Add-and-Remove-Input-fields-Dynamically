![Product Screen Shot][product-screenshot] <br/>

<!-- Demo Screenshot -->
[product-screenshot]: Screenshot.png
### Dynamic Form Input Handler

A simple HTML and jQuery solution to dynamically add and remove input fields in a form. This functionality is useful for forms requiring variable amounts of data input, such as name-value pairs.

## Features
- Dynamically add new input rows.
- Remove specific input rows.
- Real-time updates to the form layout.

## Setup and Workflow

### Step 1: Setup the HTML Structure:

Create a basic HTML form with the following elements:
- An initial input section (`#rowsection`) for entering `Name` and `Value`.
- A button (`#addrow`) to dynamically add new input rows.
- A container (`#newinputsection`) where dynamically added rows will be appended.

### Step 2: Add New Input Rows:

The #addrow button listens for a click event.
* On click, it generates a new block of HTML (newRowAdd) containing:
- A (`Name`) input field.
- A (`Value`) input field.
- A Remove button to delete the row.
* The generated HTML is appended to the #newinputsection container.

### Step 3: Remove Input Rows:

* Using (`$("body").on()`), a click event listener is attached to dynamically added #removeRow buttons.
* On click, the (`parents("#rowsection")`) is targeted and removed, deleting the associated input group.

### Built With
* Html 
* CSS
* jQuery

**HTML Example:**
```html
<div id="rowsection">
  <input type="text" name="name[]" placeholder="Enter Name">
  <input type="text" name="value[]" placeholder="Enter Value">
  <button id="addrow">Add Row</button>
</div>
<div id="newinputsection"></div>


