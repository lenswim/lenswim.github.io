---
layout: post
title:  "Docusaurus"
date:   2025-12-24 11:25:31 +0100
categories: documentation log4brains docusaurus
---

- [What problem does this Docusaurus solve?](#what-problem-does-this-docusaurus-solve)
- [How does Docusaurus differ from Log4brains or Jekyll?](#how-does-docusaurus-differ-from-log4brains-or-jekyll)
- [Is it searchable?](#is-it-searchable)
- [Example](#example)


## What problem does this Docusaurus solve?
**My problem**: I want the documentation to be close to the code and versioned.

I also want the documentation to have a human-readable form and it should be searchable.

Log4brains is a solution for this problem, but only specifically for ADR (Architecture Design Records).

**But** ...there is also [Docusaurus](https://docusaurus.io)

Similar to Log4brains you need 3 things for this:
* installing Docusaurus in your project
* a github actions workflow to build and publish the site
* github pages enabled on your repository

## How does Docusaurus differ from Log4brains or Jekyll?
While all three are Static Site Generators, they turn Markdown files into a website

They focus on different parts of the developer experience:

* **Jekyll** is the classic "Simple & Stable" choice. It’s perfect for personal blogs and basic websites because it’s baked directly into GitHub Pages.

* **Log4brains** is your "Architecture Specialist." It doesn't just display files; it understands the relationships and timeline of your decisions.

* **Docusaurus** is the "Modern Documentation Powerhouse." It’s built on React, turning your docs into a high-performance web app with advanced features like versioning and search.

## Is it searchable?
Not out-of-the-box, but there are plugins you can apply.

## Example
[CQRS Documentation](https://lenswim.github.io/cqrs/)
