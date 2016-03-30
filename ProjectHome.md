## What it is ##

A usability technique for web browsers that allows you to show floating content over other content.

![http://sublog.subimage.com/files/submodal-small.gif](http://sublog.subimage.com/files/submodal-small.gif)

Created and maintained by Seth @ [Subimage LLC](http://www.subimage.com).

## Demo ##

If you wish to see subModal in the wild take a look at Cashboard [Cashboard time tracking software / invoice software](http://cashboardapp.com) - or check out [this Ruby on Rails shopping cart](http://substruct.subimage.com). (Click the _Cart_ link)

Otherwise, [you can download the latest zip archive](http://code.google.com/p/submodal/downloads/list). It contains a working demo and example code.

## How it works ##

The subModal works by placing a semi-transparent div over the browser, blocking access to the content below while still providing visibility. This maintains state and doesn’t make someone feel disoriented or lost by moving them completely to another page. Their frame of reference is kept while allowing them to perform a new task (usually closely associated with the content below).

Another div is layered and centered on top of the mask. This div contains an iframe which defaults to a “now loading” page. In my applications I usually place an animated gif inside of this page to make it appear the server is doing something while the user waits.

Finally the iframe’s source is swapped with the page you wish to display. When this page is loaded into the iframe it’s title is swapped with our fake title bar and displayed.

Note that this works best when used in concert with a scrollable div underneath. All of my apps make use of this layout technique. It’s rare that the browser window scrolls. This code supports scrolling the entire browser window, but I don’t recommend it.

## Where it works ##

  * IE 6+
  * FireFox 0.9+
  * Safari
  * Opera 7+

_Opera 7 works in a hacked fashion._ Since Opera’s css support doesn’t include opacity I’m using a 24 bit transparent PNG file for the demo. If you don’t care about Opera you can comment this out and it will still work in FireFox, IE, and Safari. I like that method better since you have full control over the mask color and opacity right from the CSS file.

## Links of interest ##

  * [How to use SubModal](HowToUse.md)
  * [Callback functions with SubModal](UsingCallbackFunction.md)
  * [Discuss SubModal on Google Groups](http://groups.google.com/group/submodal)
  * [History of the SubModal](http://sublog.subimage.com/articles/2006/01/01/subModal)