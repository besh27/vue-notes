# Directives

- v-text
- v-html
- v-show
 - v-show will set the element style to 'display: none' until condition is met. 
- v-if
    is a conditional that will display information depending on meeting a requirement. This can be anything: buttons, forms, div, components
  - v-if will mount the component when the condition is met. 
- v-else
  - conditionally render just like v-if.
- v-else-if
- v-for
    - Loops through a set of values or static number
    ```javascript
        <ul>
            <li v-for="num in 5">{{ num }}</li> // 1,2,3,4,5
        </ul>
    ```
- v-on
- v-bind
  - one of the most useful directives so theres a shortcut! We can use the : to bind dynamic props. 
- v-model
    - Created a relationship between the data in the instance/component and a form input, so you can dynamically update values. 
    ```javascript
    new Vue({
        el: 'elName',
        data(){
            return{
                message: 'This is a good place to type things.'
            }
        }
    })
    ```
    ```html
    <div id="app">
        <h3>Type here</h3>
        <textarea v-model="message" class="message" rows=5 max-length="72"/>
        <br/>
        <p class="booktext">{{ message }}</p>
    </div>
    ```
- v-pre
- v-cloak
- v-once


---

## Modifiers

- `v-model.trim` will strip leading or trailing whitespace from the bound string.
- `v-model.number` changes string to number inputs
- `v-model.lazy` - won't populate the content automatically, it wil wait to bind until an event happens. (it listens to change evens instead of input)
