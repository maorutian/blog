---
title: Webpack VS Vite 
date: 2022-03-29 16:06:13 
tags:
---
## Module Bundler

Webpack and Vite both are module bundlers which take multiple JavaScript files and combine them into a single file that can run in the browser.

## How does Webpack work?

![Webpack](/uploads/Webpack-VS-Vite-01.png)

<!-- more -->
Webpack bundle your entire JavaScript modules, then launch the dev server, processes all the modules before a single browser request.

## How does Vite work?

![Vite](/uploads/Webpack-VS-Vite-02.png)
Vite launch the dev server first, only bundle and processes your dependency modules before a single browser request. This is why Vite is able to process your development build faster than Webpack. As your application grows, the amount of time needed to process your development build will increase at a slow rate.
**Note**
Why can vite can just converts the files which are in use? 
The availability of native ES modules in the modern browser.

## My thoughts

Vite enhances the experience of developers in development environment. They don't have huge difference in production environment. The biggest problem for Vite right now is that it doesn't have a good community for developer. It is too new, if you have a problem, it is easy to find an answer for webpack; for vite, mostly you have to figure it out by yourself. I might give it a try in development environment and keep using Webpack in the production environment.

