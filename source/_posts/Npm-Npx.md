---
title: Npm & Npx
date: 2020-08-12 16:04:44
categories: 
- Javascript
tags:
- Javascript
---
We know `npm` is a package manager, we caninstall node.js packages using npm. But what is `npx`?
I guess that everyone is confused when we start to learn React and see this code

```
npx create-react-app my-app
```

Let talk about `npx` and see what is the difference between npm and npx.

<!-- more -->

### What is NPX?
* NPX is a tool to execute node.js packages. X means Execute.

* NPX uses the packages directly from npm registry, no global or local installation required.

### When to us NPX?

#### Install packages neither globally nor locally

Sometimes, we don't want to install packages neither globally nor locally, like initiating project. For example, if we want to install `create-react-app`, we need use `npm -g` to install it globally. But we only need it when initiating project. It is a waste to install globally.
When we use npx, it downloads create-react-app to a template folder and delete it after install.

#### Execute commands directly in Terminal like testing

For example, we want to test our code using `Mocha`, we are going to check the version of our `Mocha`.
##### without NPX

```bash
./node_modules/.bin/ mocha --version
```

##### with NPX
it create a new shell to run the command.
```bash
npx mocha  --version
```
Much better!

