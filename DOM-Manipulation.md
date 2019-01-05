- [] **What is DOM manipulation?**
The DOM is the structure a web browser generates from an HTML file. The browser reads the HTML file and generates 
a version of the elements that is formatted for your JavaScript code to communicate with. We need this “translated” version
of the HTML so that we can use JavaScript to talk to the elements on the page. 
If JavaScript could not talk to the DOM, we wouldn’t be able to use JavaScript to change the appearance of the page.


When a web page is loaded, the browser creates a Document Object Model of the page, which is an object oriented representation
of an HTML document, that acts as an interface between JavaScript and the document itself and allows the creation of dynamic
web pages.

Manipulating/Changing the DOM means using this API to change the document (add elements, remove elements, move elements
around etc...).
Traversing the DOM means navigating it - selecting specific elements, iterating over groups of elements etc...

The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs
can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way,
programming languages can connect to the page.

hen a web page is loaded, the browser creates a Document Object Model of the page.

The HTML DOM model is constructed as a tree of Objects:
With the object model, JavaScript gets all the power it needs to create dynamic HTML:

- [ ] **Try to write an HTML & JS file that:**
will be loaded later


- [ ] **Why should we always use eventListeners in Javascript and not inline onClick handlers in the HTML?**
1. addEventListener does not overwrite existing event handlers on elements, whereas onclick overrides any existing 
onclick = function event handlers.

addEventListener allows you to have multiple listeners for the same event, while you cannot have multiple onclick properties.

You should probably prefer addEventListener unless you can guarantee no one is ever going to try and use onclick 
(or whatever event you're using) and override your event handler.




