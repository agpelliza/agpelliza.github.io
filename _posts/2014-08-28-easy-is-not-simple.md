---
layout: post
title: Easy is not Simple
category: guides
---

{{ page.title }}
----------------

<p class="meta">28 Aug 2014 - Buenos Aires, Argentina</p>

It often happens that we mistake simple with easy, but them are very different. A simple thing is so even when it results hard, but an easy thing depends on who is considering it. It’s a matter of objectivity versus relativity. For saying, adding new features to our software by the adoption of several tools and conventions could be really easy, but hardly simple.

Because of the many available tools, adding features could become so easy that we forgot to weigh the value them provide with the price our application has to pay for adding it. We, programmers, use to know all the tool’s benefits and ignore all the costs. Often this rise to the limit that we need to rely on tools to handle tools, what results on more complexity.

There is a particular kind of complexity associated to dependencies, and it's that programs make assumptions. Even when we try to keep them at the minimum, some remain. So when we add libraries, we also adopt their assumptions. Optimally we should understand them, and even so, the freedom to combine our software with other tools will be compromised.

There is a natural dichotomy between completeness and simplicity, as more complete something is less simple it becomes. But we mostly care all about what software does disregarding how it does it. It’s important, but hard, to find the adequate balance between simplicity and the features a program provides.

In software, staying simple usually leads to more robust and maintainable solutions. This has to do with the less LoC and dependencies, a measure that only seems to be appreciated by those embrace simplicity. But large code depending on many libraries is hard to understand, and we can only hope to make reliable the things that we understand.

From time to time, libraries fail. Most of us have faced a bug in a library and find ourselves fixing a third party’s tool. Likely, for a bug completely unrelated to our use case. This use to be the result of a complex tool trying to fix every use case, and having one of them screwing them all.

There is always the pressure to add more and more features to our software. Most of the time these features solve very specific problems that would be better to handle apart, without polluting our main program. It's possible to say “No” to a customer, I may even say that it should be the default answer.

In order to focus on our business we build abstractions that wrap solutions to provide a simpler interface, this adds complexity but in a controlled manner. For saying, an object is a complex artifact, it holds data, behaviour and maintains a state, but it provides a cleaner way to model many domains. Though, to be complex is not to be bad, there is always a trade off between complexity and the ease it provides.

Sometimes we can't stay simple, sometimes complexity is inherent to the problem and we have to deal with it, likely, by adding more complexity. When we do so, we should understand the impact to the whole program. Perhaps it's possible to split the solution on several simpler ones, or even avoid providing the feature at all. Remember, you can say no.

To conclude, tools and abstractions can be of great help and may be easy to use, but them ship with the load of complexity. Another IDE or framework claiming to solve all your needs is doubtedly the answer to your prayers, but another source for cheap, low quality software. So, use them wisely and stay simple ever possible.

[Keep it simple stupid](http://en.wikipedia.org/wiki/KISS_principle) ;-)