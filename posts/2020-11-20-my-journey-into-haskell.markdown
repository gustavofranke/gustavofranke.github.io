---
title: 'My journey into Haskell'
description: How I started my Haskell journey
tags: haskell
---

Surveying the landscape:
--------------------------

The Haskell ecosystem is an amazing piece of research and engineering; it's widely used in academia, and it has been seeing a steady adoption in [industry](https://github.com/erkmos/haskell-companies) to solve [really complex problems](https://github.com/github/semantic/blob/master/docs/why-haskell.md).

When someone starts acquiring the skill, it is through the language first. Once you get familiar with it, you will also need to learn how to build a project, and use some libraries, linters, formatters, automatically test your code, as well as have some development workflow that works for you.

Haskell happens to be a 30 year old language, started by a research group. You can imagine that this sole fact could imply some [rough](https://twitter.com/EncodePanda/status/1211433804063223809) [edges](https://www.snoyman.com/blog/2020/10/haskell-bad-parts-1) and an enormous baggage of decisions made that have changed the landscape of programming languages as well as others that have been proven bad or far from ideal. A lot has happened in the world in 30 years, and so in Haskell too.

Now, Haskell is [not quite a mainstream language](https://www.youtube.com/watch?v=iSmkqocn0oQ).
For people proficient in other languages, the discussions happening in social media could look strange, with very different concepts and terminology - leaving Haskell looking like a hard and complicated language, or even esoteric perhaps.

It’s been argued that social media makes Haskell seem much [harder to learn than it really is](https://patrickmn.com/software/the-haskell-pyramid/).
Essentially, expert users of the language that know their fundamentals very well, exchanging ideas about the state of the art of some obscure feature or technique or concept, etc.

But the truth of the matter is that you don’t need to be an expert in the language to use it. Or to accomplish interesting things in it.
What you need to understand is that this is just a very different language, not hard or complicated. This means that some of your previous programming experience might not be useful to pick things up quickly. Some of them might, but definitely not all.

When I say family of languages, I’m referring to the family of **imperative** languages, and the family of **declarative** languages.
They differ in how they compute things. In both cases, their core concepts to perform a computation, as well as the concepts to glue together a number of them are completely different.

In **imperative** programming, the basic method of computation is changing stored values. These are also more mainstream, with more industry adoption.
In **declarative** programming, the basic method of computation is the application of functions to arguments. These are less mainstream, with less industry adoption.

Ideas coming from **declarative** programming have influenced enormously latest versions of languages like Python, Javascript, C#, Java, and others. And vice versa, [Python's doctest](https://hackage.haskell.org/package/doctest), [Ruby's RSpec](https://hackage.haskell.org/package/hspec), [Smalltalk's SUnit](https://hackage.haskell.org/package/HUnit) are examples of ideas percolating into Haskell from other language communities.

Haskell falls under a flavour of **declarative** programming where functions occupy the central role; as opposed to procedures or subroutines, like in **imperative** languages.
A function is a binary relation between two sets that associates every element of the first set to exactly one element of the second set.

My journey into Haskell:
------------------------

I think I wrote my first lines of Haskell around mid 2015, while reading [**Learn You A Haskell For Great Good**](http://learnyouahaskell.com/), I used to play with the code in a very disorganised way, some times directly in the REPL, sometimes in files via `runhaskell`.
By typing code examples myself, I forced myself to face compiler warnings and compiler errors that were unfamiliar to me. Once that was passed, if curiosity kicked in, I would run little experiments by modifying the program, and re-run it to see what happens.
I remember bloating single files with lots of code, so that one simple `:load` in the REPL would type check everything. I did that because I was exploring the language, and didn’t really want to get distracted with build tools or things along those lines. This approach clearly doesn’t scale and things become crazy quite quickly. Not that I'm recommending this, it's a bit of a stretch, but at least at the start, it got me focused on the language, and craving a lot for a build tool.

Then I tried and failed many times to get familiar with [Cabal](https://cabal.readthedocs.io/en/latest/), and then [Stack](https://docs.haskellstack.org/en/stable/README/). But things didn’t quite work for me, until I found [this blog post](https://howistart.org/posts/haskell/1/) which was a great start. Seriously, I can't stress enough how much that blogpost unlocked for me, you should give it a try. Follow the steps from it, and then move on to tackle some project of your own that you might have in mind.
Now I was able to look into all those things I mentioned before, that any codebase would require (build a project, add libraries, linters, formatters, test the code).

At this point, my local development environment was a text editor, not much more. Stack has a `—file-watch` option. So, as a Haskell beginner, this provided me fast enough feedback, and IDE-like features weren’t strictly necessary.
It’s only very recently that I’ve discovered the [Haskell for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=haskell.haskell) extension, and I’m pretty happy with it. I installed it, and it just worked.

Back to **Learn You A Haskell For Great Good**, the book; it has helped a lot of people to get started with Haskell the language. But while most introductory texts come with lots of exercises, **Learn You A Haskell For Great Good** explains things in a friendly writing style, the code consists of somewhat trivial examples, to show you the syntax and basic building blocks. I think that’s a good thing, it also introduces you to modules, basic command line apps, as well as reading and writing files. Once you’re finished with it, this begs the question - what next? Read another book? I’m not a fan of reading, but I read a lot when I don’t quite know what my next step is, and that is very often. So I took up [**Programming in Haskell 2nd Edition** by Graham Hutton](http://www.cs.nott.ac.uk/~pszgmh/pih.html)

This is an amazing book, I’m a big fan of it. The content overlaps in many areas, but the extended examples are non-trivial (at least for learners), and it comes with lots of exercises too.
While I did type all the code myself, and turned it into a project, with modules, doctest and things like that. I still haven’t finished the exercises, but I clearly intend to.

It is at this point when I’m really fed up with reading about Haskell. It seems like one can read entire books and still not know how to develop in Haskell. As a programmer, I had an itch to write lots of code, so I took up the [99 Problems](https://wiki.haskell.org/H-99:_Ninety-Nine_Haskell_Problems).
There is a lot of fun in those, and you know one learns to write code by writing code, after dealing with a few of those problems I felt that I was finally getting the hang of it, and also sort of familiar with the syntax.
Am I proud of that code? No, not at all. I'm sure there are better solutions to these problems out there than mine. But at least it kept me going. It was fun. This time it wasn’t just passive reading because I didn’t know what to do next, or because every time I sat to learn a build system for Haskell things didn’t work for me.

Speaking of which, the other day I found [this code I wrote](https://gist.github.com/gustavofranke/ae05845f2082c8d8f7ded8f25ae23b96) for the fizz buzz problem, only to find [a blog post](https://www.parsonsmatt.org/2016/02/27/an_elegant_fizzbuzz.html) with a much better and idiomatic solution than mine, that also exploits some cool mathy aspects, with a much more idiomatic result.

If for some reason you’re curious, these are the Haskell toy projects I mentioned before, on GitHub:

 - [https://github.com/gustavofranke/hutton](https://github.com/gustavofranke/hutton)
 - [https://github.com/gustavofranke/ninety-nine](https://github.com/gustavofranke/ninety-nine)
 - [https://github.com/gustavofranke/lens-exercises](https://github.com/gustavofranke/lens-exercises)
 - [https://github.com/gustavofranke/rest-api](https://github.com/gustavofranke/rest-api)

There are lots of interesting introductory books. These days, the go-to one seems to be the [**Haskell Book**](https://haskellbook.com/). While I haven’t read it, I’ve seen that it’s written in a very welcoming style, and the highlights are Property Based Testing with the QuickCheck library, Monad Transformers Library, lambda calculus, with lots of examples and exercises.

I remember reading somewhere that when it comes to intermediate or advanced Haskell, all knowledge is scattered around in blogposts. There are people working very hard to change this.
But when it comes to blogposts on Haskell, content coming from these authors (in no particular order) has helped me understand things a little (actually, a lot) better:

 - [https://www.stephendiehl.com/](https://www.stephendiehl.com/)
 - [http://www.haskellforall.com/](http://www.haskellforall.com/)
 - [https://www.parsonsmatt.org/](https://www.parsonsmatt.org/)
 - [https://kowainik.github.io/](https://kowainik.github.io/)
 - [https://williamyaoh.com/](https://williamyaoh.com/)
 - [https://lexi-lambda.github.io/](https://lexi-lambda.github.io/)
 - [https://chrispenner.ca/](https://chrispenner.ca/)
 - [https://typeclasses.com/](https://typeclasses.com/)

Other resources include podcasts too, the ones I’m normally up to date with are:

 - [http://corecursive.com/](http://corecursive.com/])  
 - [https://haskellweekly.news/podcast.html](https://haskellweekly.news/podcast.html])  
 - [http://www.haskellcast.com/](http://www.haskellcast.com/])  

A few closing thoughts:
-----------------------

Practice doesn't actually make perfect, perfect practice makes perfect.

For our intents and purposes, that seems to be **focused practice writing code**.

It's easy though, to get too frustrated or too over-tired. I try to have more than one project on the go at a time, so I can switch back and forth, think a little more about things, and then come back after a while.

Read a lot, I wish I knew how to avoid this. However, you can find that [long time Haskellers](https://www.stephendiehl.com/posts/essential_haskell.html) publishing [their reading lists](https://github.com/cohomolo-gy/haskell-resources) and these are not short.

I think there’s [a lot more to get](https://williamyaoh.com/posts/2020-01-11-road-to-proficient.html) from books like **Learn You A Haskell For Great Good** and **Programming in Haskell 2nd Edition** than just reading them. The starting point for this is to play with the code in a more project oriented way, from within what a build tool has to offer, making it closer to a real world codebase.
