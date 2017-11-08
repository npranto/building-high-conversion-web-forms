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
* There are many different input types available with [HTML5](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) (i.e., time, date, url etc.). Take advantage of these formats to create better form filling experience for users
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
    
    
###### Importance of a Structured Form
* Make sure to plan out the entire process of a form filling rather than just adding some input fields and a submit button
* Draw out the entire flow and steps for a form and make sure it provides a clear, simple, fluid experience for your users (a badly structured form can affect your users)

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
* On a landscape view, labels should be next to its inputs and on a portrait view, labels should be on top of inputs    
* Avoid putting labels underneath inputs, so that it does not get hidden by keyboards and users can see label while filling  
  
###### Using Placeholders
* Usually, placeholders are provided to set good example input values for your users
* It also can work as a replacement for labels

###### Using Autofill for Auto Completion
* Autofill really makes it easy for users to auto complete a form quickly.
* Enabling auto complete lets the browser look up previously provided information to help users autofill the input values automatically
    ```html
      <form action="#">
          <label for="email">
              <span>Email:</span>
              <input type="email" id="email" autocomplete="email" placeholder="Email">
          </label>
          <label for="tel">
              <span>Email:</span>
              <input type="tel" id="tel" autocomplete="tel" placeholder="Telephone Number">
          </label>
      </form>
    ```
    
###### Using Autofocus
* Using autofocus helps the users quickly focus on input field of a form as soon as the page loads.
    ```html
      <form action="#">
          <label for="email">
              <span>Email:</span>
              <input type="email" id="email" autocomplete="email" autofocus placeholder="Email">
          </label>
      </form>
    ```
    
###### Using Validation
* Validations can be very crucial when it comes to sensitive or detailed information
* It basically provides a way for users to know whether or not they are filling the form properly
* It provides great direction and guidelines for solutions to validation errors 
* We can set both build in validation for inputs ("max", "minLength", "required") or custom validations as choose with [setCustomValidity()](https://developer.mozilla.org/en-US/docs/Web/API/HTMLSelectElement/setCustomValidity)
