
## JavaScript and jQuery book by Jon Duckett pages 293-301, 306-331 and 354-357:

* jQuery offers a simple way to achieve a variety of common
JavaScript tasks quickly and consistently, across all major
browsers and without any fallback code needed.
* Function(Creates jQuery Objects) , $(li.hot)
* jQuery doesn't do anything you cannot achieve with pure JavaScript.
It is just a JavaScript file but estimates show it has been used on over a
quarter of the sites on the web, because it makes coding simpler. 
* jQuery has methods that offer web developers
simpler ways to perform common tasks, such as:
• loop through elements
• Add I remove elements from the DOM tree
• Handle events
• Fade elements into I out of view
• Handle Ajax reques
* jQuery's motto is "Write less, do more," because it allows you to achieve
the same goals but in fewer lines of code than you would need to write
with plain JavaScript. 
<br><br>

## A matched set/JQUERY selection
* returned in jQuery can be single or multiple.
* we can use it to get and set data.
* when you create a selection with jQuery it stores a reference to the corresponding nodes in the DOM tree. It does not create copies of them.
* In plain JavaScript, if you wanted
to do the same thing to several elements, you would need to write code to loop through all of the elements you selected.
With jQuery, when a selector returns multiple elements, you can update all of them using the one method. There is no need to use a loop. 
$('l i em') .addClass('seasonal ') ;
$( ' li .hot') .addClass('favorite'); 
* CHAINING : In this one statement, three methods act on the same
selection of elements: hide() hides the elements delay () creates a pause
fade In () fades in the elements ,
$( 'l i [i d!="one"] ') . hide() .delay(SOO) . fadeln(1400); 

* checking the page is ready to  work with : <br>
![img](https://prakashdrupal.files.wordpress.com/2017/01/document-ready_.png)
<br>
<hr>
<hr>

### GETTING ELEMENT CONTENT
* . html() When this method is used to retrieve information from a jQuery selection, it retrieves only the HTML inside the first element in the matched set, along with any of its descendants.
* . text() When this method is used to retrieve the text from
a jQuery selection, it returns the content from every element in the jQuery selection, along with the text from any descendants.
* .replaceWith() This method replaces every element in a matched set with
new content. It also returns the replaced elements. 
*  . remove() This method removes all of the
elements in the matched set .
<br>
<br>

### Changing elements
* .before() This method inserts content before the selected element(s) . 
* after() This method inserts content after the selected element(s).  
* .prepend() This method inserts content inside the selected element(s),
after the opening tag 
* .append() This method inserts content inside the selected element(s),
before the closing tag. 

<br>
<br>

### GETTING AND SETTING ATTRIBUTE VALUES 
* .attr() This method can get or set a specified attribute and its value.
To get the value of an attribute, you specify the name of the attribute in the parentheses. $( ' li#one').attr('id'); 
* . removeAttr() This method removes a specified attribute (and its value). You just specify the name of the attribute that you want to remove from the
element in the parentheses. $('1 i #one') . removeAttr (' i d' };  
* . addClass() This method adds a new value to the existing value of the class attribute. It does not overwrite existing values. 
* .removeClass() This method removes a value from the cl ass attribute, leaving any other class names within that attribute intact.  




<hr>
<hr>

## ways to include jQuery in your page 
* Loading jQuary from CDN.
* The position of <scri pt> elements can affect
how quickly a web page seems to load. 
* 