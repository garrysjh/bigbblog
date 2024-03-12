---
author: Garry Shi
pubDatetime: 2024-03-12T14:05:00Z
title: Spending time Reading on Functional Programming and Trying out Gleam
slug: functional-gleam
featured: false
draft: false
tags:
  - software
  - learning
  - languages

description: My personal experiences looking at functional programming and trying out Gleam, a new functional programming language that combines simplicity with a friendly compiler, running simple programs on the terminal.
---

_Of course, like most articles, I'll probably come back to this in due time!_

## Preface

Personally, I haven't had much experience with functional languages as compared to imperative programming languages, especially since most of my universtiy education has its roots in more object-oriented languages such as Java. However, I recently came across a video [here](https://www.youtube.com/watch?v=_I-CSgoCgsk) by a Youtuber called Theo talking about the release of Gleam. It made me interested, so I spent one of my evenings after my internship taking a look at Gleam. I don't intend on spending hours becoming a Gleam master, but it is certainly interesting to take a look at newer technologies!

![Gleam's Landing Page](@assets/images/gleam/gleam-webpage.webp)
_Gleam's landing page, also found at [this link](https://gleam.run/)_

Of course, I did my research first on Reddit and a bunch of other sides apart from watching the video, and I recognize that Gleam's a fresh, new and relatively immature language compared to older functional languages such as OCaml, Elixir or Scala, and therefore would have less support online when it comes to documentation and help but I figured that I was just going to try experimenting with a new technology. Either way, I might or might not eventually try attempting a project with Gleam and document the process!

# Functional Programming

Naturally, before trying out Gleam, I did a read up on functional programming. I've read programming textbooks that mention that Functional Programming is based off of Lambda Calculus, and is has its roots in Mathematical functions.

Interestingly, one of the main proponents of functional programming is pure functions, where there are no side effects and results are deterministic such that functions written this way are easier to parallelize. One of the things I remembered about pure functions were that they are much easier to make unit tests for since you are aware of the entirety of the function. In a way, pure functions are stateless and deterministic.

## Tutorials

I went through a small portion of the [Gleam Language Tour](https://tour.glem.run/basics), and one of the most interesting parts I noticed were how the language handled types and printing.

For example, the tutorial mentioned 2 ways of "printing" to a console, with a function from their io library called `io.println` and `io.debug`, for which `io.println` only supports strings while `io.debug` supports multiple data types.

One thing I enjoyed was the compiler; where in the tutorial it was comprehensive in checking whether variables were used or type of variable at first look.

Gleam also has a type checking similar to Python3, where variables can be written with type annotation purely for documentation but are not enforced at compile time or runtime. e.g. `let _FirstName: String`

Another interesting thing was that their built in lists were immutable single-linked lists, but that also made them efficient to add and remove elements from the front of the list.

At the moment, this is all I have tried out, but I intend on continuing trying out and maybe finishing the tour / Reading up more heavily on functional programming given enough time!

[https://tour.gleam.run/basics/blocks/]: #
