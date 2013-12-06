# Context Scoping

One of the most challenging tasks we have to undertake in our quest to become expert JavaScripters is developing an understanding of _how scoping works_, how to manipulate the `this` keyword, and actually being able to tell what the value of `this` will be in a given call stack. In section `5.1.3` we talk about scopes, `this`, the `.apply`, `.call`, and `.bind` methods, as well as the `new` operator.

- [Scoping `this`](https://github.com/bevacqua/buildfirst/tree/master/ch05/03_context-scoping/scope-this.js)
- [Object Property](https://github.com/bevacqua/buildfirst/tree/master/ch05/03_context-scoping/object-property.js)

![chaos.gif][1]

## [Call, Apply, Bind](https://github.com/bevacqua/buildfirst/tree/master/ch05/03_context-scoping/call-apply-bind.js)

- `Function.prototype.call` takes any number of arguments, the first one is assigned to `this`, and the rest are passed as arguments to the function that's being invoked.

- `Function.prototype.apply` behaves very similarly to `.call`, but it takes the arguments as a single array with every value, instead of any number of parameter values.

- `Function.prototype.bind` creates a special function which can be used to invoke the function it is called on. That function will always use the `this` argument passed to `.bind`, as well as being able to assign a few arguments, creating a curried version of the original function.

## That `strict` mode

If our code is running in strict mode, then `this` will default to `undefined`, instead of `Window`. Outside of strict mode, `this` is always an object: the provided object if called with an object reference; its boxed representation if called with a primitive boolean, string, or numeric value; or the global object (again, `undefined` under strict mode) if called with either `undefined` or `null`. The value passed as `this` to a function in strict mode isn't boxed into an object. In Chapter 7, we'll learn more about what strict mode can do for us.

You can find more information about the topic on a blog post I wrote: [Where does this keyword come from?](http://blog.ponyfoo.com/2013/12/04/where-does-this-keyword-come-from "Where does this keyword come from? on Pony Foo")

  [1]: https://raw.github.com/bevacqua/buildfirst/master/images/chaos.gif "Not the prettiest of JavaScript faces"