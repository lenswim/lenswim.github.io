---
layout: post
title:  "Static Site Generators"
date:   2025-12-28 14:45:31 +0100
categories: SSG jekyll docusaurus HTML
---

- [What do Static Site Generators do?](#what-do-static-site-generators-do)
- [What is hydration?](#what-is-hydration)


## What do Static Site Generators do?

In a normal Single Page Application, the developer builds a "shell" where the browser does all the work: when a user visits, the browser receives a nearly empty HTML file and must download, parse, and execute a large JavaScript bundle before any content appears on the screen.

In contrast, with a Static Site Generator (SSG) like Next.js, Gatsby or Astro, **build command that pre-renders every page into a finished HTML** file before the site is even uploaded. 

The build step typically happens on a build node in a CI/CD pipeline and not on the user's device.

Because of this, the browser can display the full content of the page immediately, only running JavaScript later to add interactivity (a process called "hydration"). 

While a normal React app is highly dynamic and easy to deploy, an SSG offers much faster initial load speeds and superior search engine optimization because search engines don't have to wait for JavaScript to see the content.

So SSG's flattens your code fancy React or Angular into the basic building blocks:
* The HTML (The "Snapshot")
* The CSS (The "Look")
* The JS (The "Brains")

## What is hydration?
When the browser finishes showing the "snapshot" HTML, it secretly downloads that .js bundle in the background. Once the JS arrives, it "hydrates" the static page. This means React "wakes up," attaches itself to the existing HTML, and turns your fancy hooks back on so the buttons actually work.