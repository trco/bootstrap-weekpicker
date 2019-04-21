# Weekpicker widget for Bootstrap 4 & Bootstrap 3

[View the demo](https://trco.si/bootstrap-weekpicker/)

### 1. Requirements

1. [Bootstrap 4](https://getbootstrap.com/)
2. [Bootstrap 4 Datetimepicker](https://github.com/pingcheng/bootstrap4-datetimepicker)
3. [jQuery](https://jquery.com/)
4. [Moment.js](https://momentjs.com/)
5. [Font Awesome](https://fontawesome.com/v4.7.0/)

**Important:** When using Bootstrap 3 use [Bootstrap 3](https://getbootstrap.com/docs/3.3/) and [Bootstrap 3 Datetimepicker](https://github.com/Eonasdan/bootstrap-datetimepicker).

### 2. Setup

1. Load the required .css and .js files from CDNs in your HTML document or download all the files and reference them from your project folder.

2. Load the **bootstrap-weekpicker.js** from **src folder** of this repository at the end of the HTML document.

**Important:** When using Bootstrap 3 load related Bootstrap 3 .css and .js files.

```html
<!-- Stylesheets -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
<link rel="stylesheet" href="https://cdn.rawgit.com/pingcheng/bootstrap4-datetimepicker/master/build/css/bootstrap-datetimepicker.min.css">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">

<!-- JavaScript -->
<script type="text/javascript" src="https://code.jquery.com/jquery-3.2.1.slim.min.js"></script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js"></script>
<script type="text/javascript" src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js"></script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.21.0/moment.min.js"></script>
<script type="text/javascript" src="https://cdn.rawgit.com/pingcheng/bootstrap4-datetimepicker/master/build/js/bootstrap-datetimepicker.min.js"></script>

<!-- bootstrap-weekpicker JavaScript -->
<script type="text/javascript" src="https://cdn.rawgit.com/trco/bootstrap-weekpicker/master/src/bootstrap-weekpicker.min.js"></script>
```

3. Create a container element where you want to generate the week picker.

Bootstrap 4 version
```html
<div class="input-group align-items-center">
    <div id="weekpicker1"></div>
</div>
```

Bootstrap 3 version
```html
<div>
    <div id="weekpicker1" style="display: inline-block; padding-left: 8px; padding-right: 8px;"></div>
</div>
```

4. Initialize the week picker in separate <script> tag after other .js files.

```html
<script type="text/javascript">
$(function() {
    var weekpicker = $("#weekpicker1").weekpicker();
});
</script>
```

### 3. Functions

#### getWeek()
Returns the selected week.
Function should be called on **weekpicker instance**. Example bellow also shows how **getWeek()** can be tied to change event fired when week is selected.

#### getYear()
Returns the selected year.
Function should be called on **weekpicker instance**. Example bellow also shows how **getYear()** can be tied to change event fired when week is selected.

```html
<script type="text/javascript">
$(function() {
    var weekpicker = $("#weekpicker1").weekpicker();

    console.log(weekpicker.getWeek());
    console.log(weekpicker.getYear());

    var inputField = weekpicker.find("input");
    inputField.datetimepicker().on("dp.change", function() {
        console.log(weekpicker.getWeek());
        console.log(weekpicker.getYear());
    })
});
</script>
```
