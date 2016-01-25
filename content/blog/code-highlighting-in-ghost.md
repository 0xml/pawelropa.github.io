+++
date = "2014-01-09T13:58:32+01:00"
draft = true
title = "code highlighting in ghost"

+++

[Ghost blogging platform](https://ghost.org/) is great. It suits my needs almost perfectly as I don't need a colossal blogging platform with millions of plugins (and security vulnerabilities) like [Wordpress](https://wordpress.com). The posts editor is top notch, really like the preview functionality.
For [Ghost](https://ghost.org/) to be perfect I needed to add two main features; comments and code highlighting. This post will be about the latter.

There are multiple choices for the javascript code which highlights syntax. I looked at [highlightjs](http://highlightjs.org), [prism](http://prismjs.com) and [SyntaxHighlighter](http://alexgorbatchev.com/SyntaxHighlighter/). The best for my blog's current theme seemed [prism](http://prismjs.com), which I eventually used.

Here is an example of what ruby code looks like with highlighting done by prism.
```ruby
hex = [(0..9),('A'..'F')]
hex.each { |x| x.each { |y| print y }}    # outputs, 0123456789ABCDEF

# declare an array of arrays
nums = [[0,1], [2,3,4,5,6,7], [8,9], ['A','B','C','D','E','F']]
binary = nums[0]                         # => [0, 1]

a = [0, 1, 2, 3, 4, 5]    # array of 6 elements
b = a.map { |x| 2**x }    # => [1, 2, 4, 8, 16, 32]
```
<br>
###Installing Prism

* Go to [prism download site](http://prismjs.com/download.html), choose one of many themes (I personally use *Default* theme, it looks nicely with my greyish, modified version of Casper theme), select languages for which you want to add syntax highlighting (you can also add plugins i.e. line numbers).

2. Download your custom made **prism.js** and **prism.css** files.

3. Now you need to upload those files onto the server which hosts your blog. Great hosting site which I use and highly recommend is [DigitalOcean](https://www.digitalocean.com/?refcode=398e0cb398b4). For upload I like to use `scp`.

```bash
$ cd /directory/where/your/prisms/files/are
$ scp prism.js prism.css your_login@servername.com:~
```

* Your files have been uploaded onto your server. Now you need to move them into your Ghost theme directory. Login and type.

```bash
$ mv prism.js /var/www/directoryghost/content/themes/casper/assets/js/
$ mv prism.css /var/www/directoryghost/content/themes/casper/assets/css/
```

* Now you need to edit `default.hbs` file which resides inside your default theme folder.
```bash
$ cd /var/www/directoryghost/content/themes/casper/
$ nano default.hbs
```
* Add this code `<link rel="stylesheet" type="text/css" href="{{asset "css/prism.css"}}" />`
on the beginning of the file, it should look similarly to this
```javascript
<meta name="viewport" content="width=device-width, initial-scale=1.0" />

<link rel="shortcut icon" href="{{asset "favicon.ico"}}">

{{! Styles'n'Scripts }}
<link rel="stylesheet" type="text/css" href="{{asset "css/screen.css"}}" />
<link rel="stylesheet" type="text/css" href="//fonts.googleapis.com/css?family=Noto+Serif:400,700,400italic|Open+Sans:700,$

// Here
<link rel="stylesheet" type="text/css" href="{{asset "css/prism.css"}}" />

```
* And this code ` <script type="text/javascript" src="{{asset "js/prism.js"}}"></script>` near the end.
```javascript

{{! The main JavaScript file for Casper }}
<script type="text/javascript" src="{{asset "js/jquery.fitvids.js"}}"></script>
<script type="text/javascript" src="{{asset "js/index.js"}}"></script>

//Here
<script type="text/javascript" src="{{asset "js/prism.js"}}"></script>

```

Now restart Ghost. If you are using [DigitalOcean](https://www.digitalocean.com/?refcode=398e0cb398b4), simply type `$ service ghost restart`.

###Testing
Edit one of your posts and add a section at the end which looks similarly to mine (when I was creating my custom prism file, I added support for `javascript` if you hadn't, simply change *javascript* into some language name which your prism version supports).
```
 ```javascript
 var x = 5;      // Declare x, give it the value of 5
 ```
```

If you done everything right you should see something similar to this.
```javascript
var x = 5;      // Declare x, give it the value of 5
```
Thats it! You have done it!
