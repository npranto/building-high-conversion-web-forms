# building-high-conversion-web-forms
A guide to building well structured forms for the web

### Efficient Forms

##### In general,
* Forms should be well guided and similar inputs should be combined if possible to create a better flow for users
* Forms should have well defined validation messages for simpler flow and less confusion
* Forms should be well structured in terms of content and screen size
* __Understand the goal...__ forms should be quick and easy to finish
* Try to limit forms if possible, otherwise at least make sure to help users out while filling with autofill or other information that you already know about the user
* Think about forms as the best, quickest way to get some info from users to provide a service

###### How to choose the best input type?
* There are many different input types available with HTML5 (i.e., time, date, url etc.). Take advantage of these formats to create better form filling experience for users
* Try to use dropdowns for smaller menu items (less than 5 preferably)
* Use datalist instead of dropdowns if you want to provide your users with both optional choices and customizable additions
    ```html
      <input list="events">   
          <!--input 'list' attribute and datalist 'id' attribute must be same-->
          <datalist id="events">  
              <option value="Party"></option>
              <option value="Meeting"></option>
              <option value="Conference Talk"></option>
              <option value="Sports Game"></option>
          </datalist>
    ```    
###### Using Labels
* Try to combine label with input whenever you can to provide clear direction and side notes for your users
* Use a container to enclose a label and input together for association
* Use "for" attribute for a label and "id" attribute for inputs to link them together; also doing that enables user to click/touch either(label or input) for any changes or updates
    ```html
      <form>  
          <!--BOTH OPTIONS ARE FINE!-->
          <!--OPTION #1    -->
          <span>Same as billing address</span>
          <label for="use-billing"></label>
          <input type="checkbox" id="use-billing">
  
          <br>
          
          <!--OPTION #2    -->
          <label for="telephone-number">
              <span>Telephone Number</span>
              <input type="tel" id="telephone-number">
          </label>
      </form>
    ```
    
