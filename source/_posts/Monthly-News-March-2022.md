---
title: Monthly News March 2022
date: 2022-03-25 11:44:25
tags:
---
# News
**[Alert: peacenotwar module sabotages npm developers in the node-ipc package to protest the invasion of Ukraine](https://snyk.io/blog/peacenotwar-malicious-npm-node-ipc-package-vulnerability/)**

# Tools
**[Shader Park: Create Interactive 2D and 3D Shaders with JavaScript](https://shaderpark.com/)**
***Comment:***
Shader Park is a library that simplifies creating procedural graphics using javascript.
With just a few lines of code, create shaders which are: Animated, Interactive and 2D or 3D.
It allows folks who aren't necessarily familiar with writing shaders to create amazing interactive 3D graphics, skipping all the difficult boilerplate and math.
It has a lot of fun examples to explore. These examples is using WebGL, I suggest using a platform that supports a modern browser to open it, safari or any ios browser may not support.

**[React Flow: A highly customizable React component for building node-based editors and interactive diagrams](https://reactflow.dev/docs/examples/overview/)**

**[MDX: Markdown for the component era](https://mdxjs.com/)**
Use JSX in Markdown Documents

<!-- more -->

# Releases
**[Prettier 2.6 Released](https://prettier.io/blog/2022/03/16/2.6.0.html)**
Prettier 2.6: new singleAttributePerLine option and new JavaScript features!
***Comment:***
Prettier is one of the most popular code formatting tools. It just released version 2.6. In this version, Single attribute per line caught my eye. This is an option to print only one attribute per line in Vue SFC templates, HTML, and JSX. This used to piss me off so much. I would have to run prettier first, then run eslint with that rule enabled. Now I can finally get prettier to do most of the work.

# Articles


**[Delightful React File/Directory Structure](https://www.joshwcomeau.com/react/file-structure/)**



**[Tao of Node - Design, Architecture & Best Practices](https://alexkondov.com/tao-of-node/)**
Author list his own rules and principles including Structure & Coding Practices, Tooling, Testing and Performance for building Node applications.
Comment:
The Structure opinion is very interesting. Most of MVC structure by technical responsibilities, the author think that a better way to structure a node application is in modules representing a part of the domain.
He also advises you not to shoehorn everything into one utility folder but create separate files and group the business logic in them.

```
// 👎 Don't structure by technical responsibilities
├── src
|   ├── controllers
|   |   ├── user.js
|   |   ├── catalog.js
|   |   ├── order.js
|   ├── models
|   |   ├── user.js
|   |   ├── product.js
|   |   ├── order.js
|   ├── utils
|   |   ├── order.js
|   |   ├── calculate-shipping.js
|   |   ├── watchlist-query.js
|   |   ├── products-query.js
|   |   ├── capitalize.js
|   |   ├── validate-update-request.js
|   ├── tests
|   |   ├── user.test.js
|   |   ├── product.test.js

// 👍 Structure by domain modules
├── src
|   ├── user
|   |   ├── user-handlers.js
|   |   ├── user-service.js
|   |   ├── user-queries.js
|   |   ├── user-handlers.test.js
|   |   ├── index.js
|   |   ├── validation
|   |   |   ├── validate-update-request.js
|   ├── order
|   |   ├── order-handlers.js
|   |   ├── order-service.js
|   |   ├── order-queries.js
|   |   ├── order-handlers.test.js
|   |   ├── calculate-shipping.js
|   |   ├── calculate-shipping.test.js
|   |   ├── index.js
|   ├── catalog
|   |   ├── catalog-handlers.js
|   |   ├── product-queries.js
|   |   ├── catalog-handlers.test.js
|   |   ├── index.js
|   |   ├── queries
|   |   |   ├── products-query.js
|   |   |   ├── watchlist-query.js
|   ├── utils
|   |   ├── capitalize.js

```

# Handmade
**[Building Table Sorting and Pagination in JavaScript](https://www.raymondcamden.com/2022/03/14/building-table-sorting-and-pagination-in-javascript)**

**[Implementing JavaScript Delay for Cookie Consent Banner](https://dariusz.wieckiewicz.org/en/implementing-js-delay-for-cookie-consent-banner/)**

**[How To Create and Validate a React Form With Hooks](https://www.telerik.com/blogs/how-to-create-validate-react-form-hooks)**

**[Writing a React Table of Contents Component](https://blog.eyas.sh/2022/03/react-toc/)**