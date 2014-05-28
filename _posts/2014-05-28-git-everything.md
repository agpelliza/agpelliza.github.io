---
layout: post
title: Git Everything!
---

{{ page.title }}
================

<p class="meta">28 Apr 2014 - Buenos Aires, Argentina</p>

First time I met Git (the version control tool) I was amazed with the flexibility it gives you to work on every commit. When you turn to Git you suddenly become the owner of your code and the tool does what is your will and not the other way round.

I was also impressed with Git's simplicity. Every command is like magic turning all over as you would expect, but that's not all.

Start managing a repository with Git is this simple:

```
$ git init  # To initialize your repository with Git management
$ touch README.md  # Do some change to the repo
$ git add .  # Collect the changes you have done
$ git commit -m "first commit"  # Commit your changes

```

The basic flow on Git is as trivial as this (lets say you have just initialized the repo and you want to start with an issue):

```
$ git checkout -b my_issue  # Creates a local branch and starts using it
$ echo "#My first issue" > README.md  # Do your work
$ git add .  # Collect the changes you have done
$ git commit -m "fix my first issue"  # Commit your changes
$ git checkout master  # Go back to the master branch
$ git merge my_issue  # Merge your changes into the master branch

```

It's that simple yet much more powerful. There are many sweet commands at Git that let you do your work in a faster and secure way. If you are interested in learning Git's beauties I suggest you to take a look at the online [Pro Git](http://www.git-scm.com/book) book. There you will find on how to get Git installed and configured on whatever platform you are running. Also, it's a complete guide to learn Git and it's commands.

As good as the [Pro Git](http://www.git-scm.com/book) book is to learn Git, I think the only way to take full advantage of a tool is to understand it's design and how it was intended to work. Here is a great [post by Tom Preston-Werner](http://tom.preston-werner.com/2009/05/19/the-git-parable.html) (Github's co-founder) with a parable on how Git works that I found particularly interesting.

But all of this are old news. What I have recently found is that Git's power goes far beyond the limits of source control. It's simplicity makes it ideal to manage any file-based working set. For saying, managing dotfiles is a fairly common usage for Git, as well as any other configuration files. It's also widely used as the basis for deploying strategies, not just for application as [Heroku](https://www.heroku.com/) does, but on static sites like [Jekyll](http://jekyllrb.com/) does or online books like [GitBook](https://www.gitbook.io/) does, among others.

A really interesting usage is to manage file-based plugins. You can keep each plugin for your application under an independent version control, then updating it is as simple as pulling the changes from the origin, and trying different version is just moving around commits.

Being such a simple, yet powerful, tool makes Git excellent to manage almost any repository you are working on. Never mind if you are working on a software application, a new plugin for your favorite editor, a new book, a post or some draft for planning your next trip. Whatever it is, having it under control gives you a lot of confidence on doing and undoing at will, trying crazy things with no harm or risk of losing your ideas. Now a days I don't even start working on anything without initializing it on Git.. Git everything!