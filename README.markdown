# listToLight.js

listToLight is a super simple lightbox script.

Most lightbox scripts require you to add classes (or other attributes) to the images that you want to be lightboxified.

This is fine, most of the time. But sometimes, you don't want to do this. If you're using Jekyll, for example, adding classes means using HTML. This is a pain - it's nicer just to use Markdown syntax.

With listToLight, any images in lists will be 'lightboxified'. This means that the list will turn into a scrollable slideshow, activated by clicking on an image. The original list will also have a class added, so that you can style the inline images appropriately (eg turning them into thumbnails).

The slideshow can be scrolled and closed using the buttons provided or using your keyboard (left arrow/right arrow/esc)

## Usage

listToLight requires jQuery, so make sure that you're using it:
    
    https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js

Include the 'ltl' directory in your static tree. Include the files comme ça:

    <link rel="stylesheet" media="screen" type="text/css" href="/path/to/js/ltl/ltl.min.css">
    <script type="text/javascript" src="/path/to/js/ltl/ltl.min.js"></script>
    
Use the following to lightboxify all images in lists:

    $(document).ready(function () {
        'use strict';
       listToLight();
    });

Use the following to lightboxify only images in lists within containers with class 'foo':

    $(document).ready(function () {
        'use strict';
       listToLight('.foo');
    });

## What it doesn't do.

Your thumbnails are just going to be your regular images, only scaled down. This isn't ideal, but in this day and age of high quality images, this isn't that big a deal. And it means no waiting to load when people do click to increase the size.