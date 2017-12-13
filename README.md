# VueJS Guide

## Show/Hide Elements
### v-show
This can be used to show/hide element based on a condition true. Please have a look at the following code.
```
  <div id="app">
    <p v-show="make == 'honda'">This offer available only for Honda Users</p>
    <textarea v-model="make" id="" cols="30" rows="10"></textarea>
  </div>
  
  new Vue({
    el: "#app",
    data: {
      make: null
    }
  });
```
### v-if
This is an alternative to v-show, except it only loads the html elment when the condition is met.

```
  <div id="app">
    <p v-if="make == 'honda'">I will only render the value is honda</p>
    <textarea v-model="make" id="" cols="30" rows="10"></textarea>
  </div>
  
  new Vue({
    el: "#app",
    data: {
      make: null
    }
  });
```
