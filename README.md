# Summernote Plugin Upload Image

Super simple WYSIWYG Editor.

### Installation and dependencies

Summernote is built on [jQuery](http://jquery.com/).

Need Install SummerNote

Include the following code in the `<head>` tag of your HTML:
```html
<!-- include libraries(jQuery, bootstrap) -->
<script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script> 
<link rel="stylesheet" href="//cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/3.3.5/css/bootstrap.min.css" />
<script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/3.3.5/js/bootstrap.min.js"></script>

<!-- include summernote css/js-->
<link href="summernote.css" rel="stylesheet">
<script src="summernote.js"></script>

```

#### 1. Include JS/CSS

It is necessary to point to the address of the upload file.
```html
<!-- include summernote plugin css/js-->
<script type="text/javascript">var SUMMERNOTE_UPLOAD = 'plugins/picture-upload/api/index.php';</script>
<link href="plugins/picture-upload/summernote-ext-picture-upload.css" rel="stylesheet">
<script src="plugins/picture-upload/summernote-ext-picture-upload.min.js"></script>
```

#### 2. Target a element

Then place a `div` tag somewhere in the `body` tag. This element will be replaced with the summernote editor.

```html
<div id="summernote">Hello Summernote</div>
```

#### 3. Add Plugin to Toolbar!

Finally, run this script after the DOM is ready:

```javascript
$(document).ready(function() {
  $('#summernote').summernote({
              toolbar:[
                  ['style', ['style']],
                  ['font', ['bold', 'underline', 'clear']],
                  ['fontname', ['fontname']],
                  ['color', ['color']],
                  ['para', ['ul', 'ol', 'paragraph']],
                  ['table', ['table']],
                  ['insert', ['link']],
                  ['view', ['codeview', 'help']],
                  <!-- add plugin -->
                  ['custom',['picture-upload']]
              ],
              height: 200,
              tabsize: 2,
              focus: false
          });
});
```


### API

`code` - get the HTML source code underlying the text in the editor:

```javascript
var html = $('#summernote').summernote('code');
```

For more detail about API, please refer to [document](http://summernote.org/getting-started/#basic-api).

### License
Summernote may be freely distributed under the MIT license.
