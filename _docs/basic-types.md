---
title: Basic Types
layout: docs
permalink: /docs/basic-types.html
---

For programs to be useful, we need to be able to work with some of the simplest units of data: numbers, strings, structures, boolean values, and the like. In TypeScript, we support much the same types as you would expected in JavaScript, with a convenient enumeration type thrown in to help things along.

###Boolean
The most basic datatype is the simple true/false value, which JavaScript and TypeScript (as well as other languages) call a 'boolean' value.

{% highlight js %}
var isDone: boolean = false;
{% endhighlight %}


###Number
As in JavaScript, all numbers in TypeScript are floating point values. These floating point numbers get the type 'number'.

{% highlight js %}
var height: number = 6;
{% endhighlight %}
