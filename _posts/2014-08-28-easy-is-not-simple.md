---
layout: post
title: Easy is not Simple
---

{{ page.title }}
================

<p class="meta">28 Aug 2014 - Buenos Aires, Argentina</p>

It's frustrating that there are lot of programmers taking the easy way while claiming for the simplest one. Most of the time the simpler and easier solutions do not match, but still, programmers pick easy as if it is simple.

There is no misunderstanding on what easy is and what it is not. But, what is to keep software simple?
It is to develop software that does one thing, and one thing only, while being context agnostic ever possible. It shouldn't do more than what you need, or provide more functionality than the strictly necessary.

There is a natural dichotomy between completeness and simplicity. As more simple you stay, less complete tools will be created. Equally, as more complete the tools more complex them will result. This is inevitable, so each one needs to find it's own balance.

Complex tools require more code and, usually, more dependencies. This leads to a different kind of complexity, the one based on the assumptions that software does.

Complete tools, in order to solve you all the problems you may have, assume several things on the context and even in what you will need to do. Also, each dependency makes it's own assumptions. This make tools hard to maintain and combine. Any change in this chain of assumptions may result in failing tools that will need to be fixed, or patched.

Fixing this tools with so many lines of code and dependencies is hard. Reading thousands of lines of code across nets of dependencies is time consuming and requires an enormous effort. Even if we expend the time and do the effort, we are at risk of breaking something else. This is because them are hard to understand, and we can only hope to make reliable, things that we understand.

To make it worse, most of the time we will find ourselves fixing problems that aren't ours, problems that we wouldn't have if we weren't using the complex tool in the first place.

When tools do assumptions them become difficult to combine. Different tools make different assumptions, and most likely those won't match.

I believe using simpler tools leads to more reliable and maintainable software. Software that anyone can understand. Simple software is easy to combine with others, even with those intended to solve a problem in a completely different context.
When you build a simple tool you will find people using it at scenarios you don't ever imagine. And that's cool.

So far we have covered tools, but there is also simplicity, and complexity, at lower levels. For saying, we are all familiar with objects, and we probably consider them simple, while them are not. Objects orientation is a complex solution. An object holds lot of concepts and responsibilities in a single piece of work. So, we make up rules to deal with them, what adds more complexity.
Don't misunderstand me, I'm not against objects but that doesn't makes them less complex.

Complexity is not necessarily bad, sometimes we can't stay simple, sometimes complexity is inherent to the problem, and we have to deal with it. The issue arise when we accept complexity without understanding it, when we add it without considering the cost, or even ignoring the fact that there is a price to pay for it. Then we lose control of our software and start relying on other tools, tools that are inevitably complex in order to deal with that complexity. From that point forward, you at the mercy of others.

Understanding the decisions we make keeps us in control of our software. Without that control we can't be confident when making changes, and the result will hardly be robustness.
If you find yourself in the need to add complexity, do it. But understand what you are doing, choose to pay that price and assume the risks to get the benefit it provides. Yes, complex tools also have benefits, I'm not saying them don't. What I'm saying is that programmers use to know all the software's benefits and ignore all the costs.

In summary, avoid complexity whenever you can. Find your balance between features and simplicity. Don't mistake simple by easy.
Regarding this last, a great way to identify when you are using easy by simple is to think in terms of objectiveness vs relativeness. A simple thing is so no matter who, while an easy thing depends on who is considering it. Something could be easy for some and hard for others, but simple is so even if it results hard.

[Keep it simple stupid](http://en.wikipedia.org/wiki/KISS_principle) ;-)