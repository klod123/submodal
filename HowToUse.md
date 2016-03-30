After downloading the code it’s as easy as including references to a couple files and inserting some HTML into your page.

At the head of your file you’ll want to add the following references…

```
<head>
    <link rel="stylesheet" type="text/css" href="subModal.css" />
    <script type="text/javascript" src="common.js"></script>
    <script type="text/javascript" src="subModal.js"></script>
</head>
```

The css contains sizing and display styles for the popup elements.

Common.js contains standard functions I find useful such as attaching event handlers and obtaining the browser’s dimensions.

subModal.js is where all the action happens. Inside event handlers are attached for the load and resize events of the browser. The load event initializes dhtml objects that are reused when showing, hiding, or resizing the window.

The javascript file also inserts any HTML necessary for the subModal.

Now that everything’s in place all you have to do is add something that’s going to call the function to show the modal.

### This is accomplished by calling the following javascript ###

```
showPopWin('your_url_here.html', width, height, null);
```

**OR by using a CSS selector like so**

```
<a class="submodal" href="modalContent.html">show modal window using class</a>
<a class="submodal-200-400" href="modalContent.html">show modal window using class and overriding default size</a>
```

The first argument is the file to load, followed by width and height (integers). Any content that overflows these dimensions will scroll inside the modal, like a real window.

The fourth argument allows you to pass a javascript function that will be called when the window is closed – by calling hidePopWin(true). hidePopWin will not call the return function by default. This is useful for cancel button functions.

## Callback ##

If you'd like to return a value or execute some other code when the window is closed, see the [instructions on using a callback function here](UsingCallbackFunction.md).