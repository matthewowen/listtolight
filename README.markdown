## NOT MAINTAINED

I hope this helps you, but I have to be honest: I'm not really working on this anymore, and so I can't rule out that there are things that don't work right etc etc etc. If you want to contribute or fork or anything, please do! But I just don't really have the bandwidth for bugfixes, let alone feature requests! Sorry :(.

# listToLight.js

listToLight is a super simple lightbox script.

Most lightbox scripts require you to add classes (or other attributes) to the images that you want to be lightboxified.

This is fine, most of the time. But sometimes, you don't want to do this. If you're using Jekyll, for example, adding classes means using HTML. This is a pain - it's nicer just to use Markdown syntax.

With listToLight, any images in lists will be 'lightboxified'. This means that the list will turn into a scrollable slideshow, activated by clicking on an image. The original list will also have a class added, so that you can style the inline images appropriately (eg turning them into thumbnails).

The slideshow can be scrolled and closed using the buttons provided or using your keyboard (left arrow/right arrow/esc)

## Usage

listToLight requires jQuery, so make sure that you're using it:
    
    <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>

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

## License and copyright

Copyright 2012 Matthew Owen

Distributed under the terms of the GNU General Public License

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
