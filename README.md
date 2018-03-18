# Weekpicker widget for Bootstrap 4

[View the demo](https://jsfiddle.net/aLgdffvs/1/)

### 1. Requirements

1. [Bootstrap4](https://getbootstrap.com/)
2. [Bootstrap4 Datetimepicker](https://github.com/pingcheng/bootstrap4-datetimepicker)
3. [jQuery](https://jquery.com/)
4. [Moment.js](https://momentjs.com/)
5. [Font Awesome](https://fontawesome.com/v4.7.0/)

### 2. Setup

1. Load the required CSS and JavaScript resources from CDNs in your HTML document or download all the files and reference them from your project folder.

2. Load the Bootstrap 4 Weekpicker's JavaScript at the end of the HTML document.

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

```html
<div id="weekpicker1"></div>
```

4. Initialize the week picker in separate <script> tag after other JavaScript files.

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
Function should be called on *weekpicker instance*. Example bellow also shows how *getWeek()* can be tied to change event fired when week is selected.

#### getYear()
Returns the selected year.
Function should be called on *weekpicker instance*. Example bellow also shows how *getYear()* can be tied to change event fired when week is selected.

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
