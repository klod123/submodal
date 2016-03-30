  1. Define the function that’ll be called on the opening page.
  1. Pass the function you’d like to call into 'showPopWin'.
  1. Assign any return value on the modal page itself, if necessary
  1. Call the hidePopWin function passing true

It might be easier to grok in code, so here's an example:


**On the SubModal opening page**

```
// returnVal can get passed in from the modal page itself...
//....see below for info
function returnRefresh(returnVal) {
  window.document.reload();
}

// Open the modal, passing in the refresh function 
// as a reference NOT a string.
showPopWin('mymodal.html', 500, 500, returnRefresh);
```

**From inside the SubModal window**

```
// If you plan to pass a return value assign it
var returnVal = "something";

// When you're ready to close the pop window 
// call this...Passing true makes sure the return 
// function gets called.
window.top.hidePopWin(true); 
```