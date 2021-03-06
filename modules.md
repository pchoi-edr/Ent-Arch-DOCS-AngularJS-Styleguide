# Modules

* Modules should be named with lowerCamelCase. For indicating that module `b` is submodule of module `a` you can nest them by using namespacing like: `a.b`.

  There are two common ways for structuring the modules:

  1. By functionality
  2. By component type

     Currently there's not a big difference, but the first way looks cleaner. Also, if lazy-loading modules is implemented \(currently not in the AngularJS roadmap\), it will improve the app's performance.

> **Bad:**

```js
var app = angular.module('app', []);
app.controller();
app.factory();
```

> **Good:**

```js
angular
  .module('app', [])
  .controller()
  .factory();
```



