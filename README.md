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

## Event Handling with VueJS
If you want to handle events with Vuejs, you can actually write a simple event handler inside your script like the one bellow.

### On Submit Event Handling

```
  <div id="app">
    <form method="post" v-on:submit="submitHandler">
        <input type='email' name='email'>
        <input type="submit" value="Suscribe">
    </form>
  </div>
  
  new Vue({
    el: "#app",
    methods: {
    	submitHandler: function(){
      	alert("You clicked the submit button!");
      }
    }
  });
```

### On Submit Event Handling - Keep it Simple
Here is another cool hack which will help you to write less code, using "@" symbol instead of "v-on:"

```
  <div id="app">
    <form method="post" @submit="submitHandler">
        <input type='email' name='email'>
        <input type="submit" value="Suscribe">
    </form>
  </div>
  
  new Vue({
    el: "#app",
    methods: {
    	submitHandler: function(){
      	alert("You clicked the submit button!");
      }
    }
  });
```

### Prevent default submit button action
The above demo will show an alert, then when you OK button of the click alert button, it will submit the form. If you want to stop this behavior you may use "prevent". Here is the updated code

```
  <div id="app">
    <form method="post" @submit.prevent="submitHandler">
        <input type='email' name='email'>
        <input type="submit" value="Suscribe">
    </form>
  </div>
  
  new Vue({
    el: "#app",
    methods: {
    	submitHandler: function(){
      	alert("You clicked the submit button!");
      }
    }
  });
```


