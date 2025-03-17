---
author: Garry Shi
pubDatetime: 2024-06-20T17:24:00Z
title: Hydrogen by Shopify
slug: hydrogen-shopify
featured: false
draft: false
tags:
  - software
  - learning
  - frontend
description: My Experience with Hydrogen by Shopify
---

## Introduction

Recently, I had the experience of working on a project with a friend for a Shopify website. Shopify currently offers 2 main options for use in designing a webpage - to use and modify their default templates or to use Hydrogen, which is their custom headless framework built on top of Remix, which is another Frontend Framework.

## Why the need for Hydrogen?

Before working on the project, the necessity of a headless framework was questioned - was it necessary to overcomplicate the process of creating a storefront online by deviating from a standard Shopify template builder? Naturally, there is a lack of creative freedom when it comes to the use of templates - you are limited by the template builder and their dev team, if the template builder doesn't allow you to modify certain elements, then you are forced to work within the boundaries of the given template builder. Naturally, one can push the boundaries of templates, but then again there is always more freedom in frontend code from scratch. 

Shopify Hydrogen advertises itself as a popular framework used by creative artists such as Drake and storefronts used by artists, and given this was the context of my friend's Shopify website, and it was an opportunity for us to learn and pick up a new technological tool, we chose to learn and adapt Hydrogen into Shopify, despite the longer development period and the extra time necessary to pick up a new technology.

![Hydrogen Ad](@assets/images/hydrogen/hydrogen.png)

## Why we chose Hydrogen?
Naturally, we did our research as well. 
1. Hydrogen prides itself as being built specifically for Shopify by working directly with Shopify’s Storefront API, reducing the need for manual API integration. This aided specifically for eCommerce which was the main usecase, and we expected the reduced need for manual API integration to speed up the development process by not having to call the API directly through http requests or Axios and instead using abstractions that are provided by Shopify themselves in the Shopify Manage Platform dev tools such as remaining quantity of items or item details. We also expected a performance boost from these API integrations through:
2. React Server Components (RSC) to improve performance by reducing JavaScript bundle sizes along with providing server-side rendering (SSR) and partial hydration out of the box. As creatives, my friend wanted to explore the use of animations and customized Javascript components in the web application, and ensuring performance was necessary for the best SEO through the best lighthouse score so that people would be able to find the store more easily.
3. Hydrogen also came with Prebuilt Commerce Components, reducing the dev time necessary to create our own components with ready-to-use UI components that we could modify more freely by editing the components directly. This allowed for easier work with unfamiliar elements such as product listings, cart management, and checkout integration.
4. Finally, Shopify also offers Oxygen, a hosting platform optimized for Hydrogen apps, which allowed for more smooth deployment with simple domain and DNS configurations, although they were not without their problems that we encountered. 
