# DOM

## What is DOM?
* The **Document Object Model(DOM)** represent the content of XML or HTML document as <ins>Tree Structure.
* DOM is a programming interface or an API, this can be used with any programming language most commonly it is used with <ins>JavaScript.
* Using DOM, we can eaisly read, access and update the contents of the document.
## How does it help?
* HTML is  used to <ins>structure</ins> the web pages while JavaScript is used to add behavior to our web pages. When HTML document is uploaded into the browser, the JavaScript can't understand the HTML document directly. So, a corresponding document is created, that is DOM.
* DOM represent same HTML document but in different format with use of objects.
* **Example:** Representation of HTML elements in tree structure.
```HTML
<table>
    <ROWS>
        <tr>
            <td>Cars</td>
            <td>Scooter</td>
        </tr>
        <tr>
            <td>MotorBike</td>
            <td>Bus</td>
        </tr>
    </ROWS>
<table>
``` 
![](https://media.geeksforgeeks.org/wp-content/uploads/DOM.png)
## Ways to access HTML elements using JavaScript:
1. ### Get HTML element by **ID**:
   * Most of developers use unique ids in whole HTML document.
   * User can use [getElementById() method](https://www.geeksforgeeks.org/html-dom-getelementbyid-method/) to access HTML element using the id.
   * **Syntax:**
   *     document.getElementById(element_ID)
1. ### Get HTML element by **className**:
   * The [getElementsByClassName() method](https://www.geeksforgeeks.org/html-dom-getelementsbyclassname-method/) is used to access the HTML elements by using **className**.
   * **Syntax:**
   *     document.getElementsByClassName(element_classnames);
1. ### Get HTML element by **Name**:
   * The [getElementsByName() method](https://www.geeksforgeeks.org/html-dom-getelementsbyname-method/) is useful to access the HTML elements using the name.
   * **Syntax:**
   *     document.getElementsByName(element_name);
1. ### Get HTML element by **tagName**:
   * The [getElementsByTagName() method](https://www.geeksforgeeks.org/html-dom-getelementsbytagname-method/) is useful to access the HTML elements using the tag name.
   * **Syntax:**
   *     document.getElementsByTagName(Tag_name);
1. ### Get HTML element by **CSS Selector**: 
   * In this, the user can select the HTML element by using CSS selectors (class, id and tagName).
   * The [querySelector() method](https://www.geeksforgeeks.org/html-dom-queryselector-method/) returns the first element that matches the particular CSS selector.
   * The [querySelectorAll() method](https://www.geeksforgeeks.org/html-dom-queryselectorall-method/) returns all element that matches the particular CSS selector. 
   * **Syntax:**
   *     document.querySelector(selectors);
   *     document.querySelectorAll(selectors);
## JS DOM helper methods 
* Objects in the DOM-Tree may be addressed and manipulated by using methods on the objects.
* Essential JavaScript DOM methods:
   * ### <ins>Node: 
      * Any element on a page including text & whitespaces of a DOM structure is known as “NODE.” Nodes can be between XHTML Tags.

      * Nodes available in DOM:

      *     node.childNodes
      *     node.irstChild
      *     node.lastChild 
      *     node.parentNode
      *     node.nextSibling
      *     node.previousSibli

   * ### <ins>createElement:
      * As the name goes, it is used to create an element & place it anywhere in the DOM structure. 
      * **syntax:**: New element will be created & added in the DOM structure.
      *     var myNewListItem = document.createElement(“li”) 
      *     var myNewProd = document.createElement(“prod5”);
   * ### <ins>appendChild:
      * Previously we created element, now we will add two elements to our list of links using appendChild.
      * **Syntax:**
      ```
      var myNewListItem = document.createElement(“li”)
      var myNewProd = document.createElement(“prod5”);

      var myLinkList = document.getElementById(“List”)
      myLinkList.appendChild(myNewListItem);
      myLinkList.LastChild.appendChild(myNewProd);
      ```
      * Above the code adds anchor tag inside of
      element at the endpoint. If we can create or append, then we can remove it too. 
   * ### <ins>removeChild:
      * Following is a code to remove Child method:  
      * **Syntax:**
      ``` var myLinkList = document.getElementById(“list”)
      var myRemovedLink = myLinkList.lastChild;
      myLinkList.removeChild(myRemoveLink);
   * ### <ins>getAttribute:
      * With the getAttribute method, you can access the value of any attribute of an element on a page. Suppose there’s an id with abc attribute having value “Best.” 
      * **Example:**
      ```
      var myLinkFive = document.getElementById(“Prod_5”);
      var myLinkAttribute = myLinkFive.getAttribute(“abc”);
      ```
      * Now getAttribute will retrieve the value from “abc,” i.e., “Best.” This method is used to target links with specific attributes & values. 
   * ### <ins>setAttribute:
      * A useful method to replace values in the attribute.    Assigning a new value to an existing attribute is done using setAttribute. Suppose we have an attribute “abc” containing value “Best.” 
      * Now we want to change the value to “Awesome.” Following is a suitable code:
     ```
      Var myLinkFive = document.getElementById(“Prod_5);
      myLinkFive.setAttribute(“abc”, ”Awesome”);
     ``` 
   
## Reference
* [One](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiB2fjlq7T5AhWsgFYBHVSQD-MQFnoECAoQAQ&url=https%3A%2F%2Fwww.geeksforgeeks.org%2Fdom-document-object-model%2F&usg=AOvVaw2q2QlQ9ibTWbr3jZfbrsYY) 
* [Two](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjy5cW4rLT5AhXugFYBHUxWDuMQFnoECA8QAw&url=https%3A%2F%2Fwww.w3.org%2FTR%2FDOM-Level-1%2Fintroduction.html&usg=AOvVaw2Z-Rm4UtgapLCGv_0FKK-t)
* [Three](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjy5cW4rLT5AhXugFYBHUxWDuMQFnoECDYQAQ&url=https%3A%2F%2Fdeveloper.mozilla.org%2Fen-US%2Fdocs%2FWeb%2FAPI%2FDocument_Object_Model%2FIntroduction&usg=AOvVaw0k54DcC1P-DYg3MIUliwmf)