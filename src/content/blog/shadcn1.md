---
author: Garry Shi
pubDatetime: 2024-03-10T09:19:00Z
title: Introduction to shadcn-ui
slug: shadcn
featured: false
draft: false
tags:
  - shadcn
  - frontend
  - ui
  - software
  - learning
  - libraries

description: My experience and opinions on shadcn
---

# Introduction

![shadcn](@assets/images/shadcn.webp)

You can find the shadcn documentation here at [shadcn-documentation](https://ui.shadcn.com/docs/installation)

## What is shadcn?

Recently, I had the time to tinker around with shadcn. Shadcn-ui is not a component library unlike normal UI frameworks, which means that components that shadcn-ui use are chunks of code that are stored locally inside your project for you to be able to use to edit at your own will. Shadcn is built on styling on top of the Radix UI and Tailwind CSS, meaning that the only dependencies used are Radix and Tailwind, and the components built are for your own personal customization.

```
import {
  Accordion,
  AccordionContent,
  AccordionItem,
  AccordionTrigger,
} from "@/components/ui/accordion"
```

For example, shadcn-ui requires the user to import components that are installed/copy-pasted with `npx shadcn-ui@latest add accordion`, and the code is now part of your source code.

## My Experience

I first found out about shadcn-ui from YouTube videos, in which it was praised as a new format type of frontend component library.

My initial experience with shadcn-ui was relatively lukewarm. I enjoyed how it was able to get things off the ground really quickly with pre-defined components with much better control.

Since shadcn-ui adds the component directly to your source code, for a relative beginner, it might be more difficult for someone to have to maintain and manage, instead of using code retrieved from within a package; However, this downside doesn't apply to that of a professional, for which one might prefer the higher customizability of components imported directly into your source code.

Embracing the beginner mindset, shadcn-ui is convenient and fast for a beginner to spin up a few components in an hour and create a working draft of a React application as fast as possible. However, perhaps for someone relatively newer to frontend UI libraries or the frontend scene in general, I'd believe that having the ability to create your own components from scratch would be a valuable learning experience and more important depending on the use-case.

I read through a bunch of discourse on shadcn, and people seemed to agree that as a beginner, one should try to implement UI components yourself without any external libraries purely for learnings sake, then afterwards use UI component libraries to save time once you want to create a working product.

I might be experimenting with shadcn-ui more in the future or similar UI components "libraries" such as Mantine and Radix, but that will be for another time!
