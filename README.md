# Vue.js

[Vue.js]()https://vuejs.org/v2/guide/ is a Javascript framework for constructing website UIs. It resembles Angular in many respects and also has certain conceptual similarities to React.

You can [download vue.js](https://vuejs.org/js/vue.min.js) to include it in your project or you can load it from a cdn:

```<script src="https://cdn.jsdelivr.net/npm/vue"></script>```

When this file loads, it will put into global scope a constructor named ```Vue```. You will call this constructor, passing it an object with configuration information, to create a ```Vue``` instance. The process of writing a ```Vue``` app is mainly adding properties and methods to the object you pass to the Vue constructor.

Let's start out by calling it with the simplest imaginable object.

```
new Vue({
    el: '#main'
});
```

The ```el``` property tells Vue what element your UI will appear in. Vue will automatically find the element that matches the selector and store it in a property of your instance named ```$el```. The contents of the element will be treated as a template and automatically rendered.

```
<!doctype html>
<html>
<head>
    <title>My Vue.js App</title>
</head>
<body>
    <div id="main">
        <p>{{ 'Hello World!' }}
        <p>2 + 2 = {{ 2 + 2 }}
    </div>
    <script src="https://cdn.jsdelivr.net/npm/vue"></script>
    <script src="script.js"></script>
</body>
</html>
```

Given this HTML, and assuming the call to the Vue constructor above is placed in script.js, the visible result would be:

