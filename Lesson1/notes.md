## HTML

```html
<div></div> <!-- division -->
<h1></h1> <h2></h2> <!-- heading 1-6-->
<p></p> <!-- paragraph -->
<em></em> <!-- emphasis (italics) -->
<strong></strong> <!-- bold -->
<a href="my-link"></a> <!-- anchor (link) -->
<img src="link-to-image.jpg" /> <!-- image tag -->

<div class="myClass"></div> <!-- Multiple use -->
<div id="myId"></div> <!-- Single use -->
```

<!-- Advanced Users -->
https://www.w3schools.com/TAGs/ - Explore using some new HTML tags
* HTML5 tags (audio, video)
* Forms
* Meta tags

## CSS

```css
div {
    color: red;
    margin: 20px;
}

p {
    font-weight: bold;
}

h1 {
    text-align: center;
}
```

<link rel="stylesheet" type="text/css" href="">

https://www.w3schools.com/Css/css_examples.asp

## Javascript

```javascript
// Overview
document.write("Hello World");
var myVariable = "some string"; //or 5 (number), or true (boolean), or array [], or object {}

var a = "This is"
var b = " concatenation."
var c = a + b; // This is concatentation

var d = 5;
var e = 5 + d++; // 10, but d now equals 6
var e = 5 + ++d; // 11, and d equals 6

var myString = "ABCDEFG"
myString.length // 7
myString.substring(0, 3) // ABC

var a = new Array(2)
a[0] = "cat"; a[1] = true;

if (condition){
    // do something
} else {
    // or do this instead
}

for(i=0; i<5; i++){
    document.write(i);
}

// self executing function
(function() {
    //console.log("Hello World");
    myFunction();
    myFunctionWithParameter("foo");
})();

function myFunction() {
    console.log("Hello World");
    //alert("Hello world");
}

function myFunctionWithParameter(param) {
    console.log(param);
}
```
<script src=""></script>

## Git and GitHub

```shell
git --version
git config --list
git config --global user.name
git config --global user.email
git config --help || git help config
mkdir, cd, ls -la (dir)
git init
rm -rf .git
git status
touch .gitignore
git add .
git commit -m "initial commit"
git remote add origin https://github.com/user/repo.git
git push -u origin master
```

## Resources
* [Git Docs](https://git-scm.com/doc)
* [Web Dev Video](https://www.youtube.com/watch?v=5YDVJaItmaY)
* [Stackoverflow](https://stackoverflow.com/)
* AWS, Digital Ocean, MS Azure, Google - Web hosting and cloud computing\
* [Most forked repos on GitHub](https://github.com/search?o=desc&q=stars:%3E1&s=forks&type=Repositories)
* [Most starred repos on GitHub](https://github.com/search?q=stars%3A%3E100&s=stars&type=Repositories)
