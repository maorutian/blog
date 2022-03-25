---
title: 'Build your own blog with Hexo and Github Pages '
date: 2020-04-29 14:17:29
categories: 
- Blog Setting
tags:
- Github Pages
- Blog
- Hexo
---

## Before Starting

### Why I want to build my own blog?
A blog can help me record all the knowledge I learned. 

### Why use Hexo and github page?
I am looking for a framework that supports markdown and the ability to host online free of charge and has support for continuous deployment whenever I check in my markdown file.
There are various popular static HTML generator frameworks available in the market, such as hugo, jeykill, and hexo. I decided to go with Hexo framework and GitHub Pages for hosting. 

<!-- more -->

### What is Hexo?
[Hexo](https://hexo.io/docs/index.html) is framework which can generate Markdown to html with a beautiful theme.

### What is Github Pages?
[GitHub Pages](https://pages.github.com/) is a static site hosting service that takes HTML, CSS, and JavaScript files straight from a repository on GitHub.

## Get Starting
### 1. Install Hexo and initialize our blog

```
# install hexo
npm install -g hexo-cli

# initialize a hexo folder called blog or whatever you want
hexo init blog

#change to blog folder
cd blog

#post first blog
hexo new post "My First Blog"

#generate the static files (html, css, etc) for your website
hexo generate

#Starts a local server. By default, this is at http://localhost:4000/.
hexo server
```

If you go to ```http://localhost:4000/``` you can see your blog now. hexo initialize a Hello World document in the blog, you can see it now.

![Blog](/uploads/Build-your-own-blog-with-Hexo-and-Github-Pages-01.png)

Hexo uses Landscape for default theme.
If you want to use the same theme like my blog, cheack this article: [Hexo Theme Next](https://maorutian.github.io/2020/04/30/Hexo-Theme-Next/) 

### 2. Deploy blog at Github Pages

#### 1) Create a new Repository in github
Create a new repository: [https://github.com/new](https://username.github.io), replace username with your own (same as Owner on the left).

![Repo](/uploads/Build-your-own-blog-with-Hexo-and-Github-Pages-02.png)

#### 2) Install Deployer Plugin

```
npm i --save hexo-deployer-git
```

#### 3) Deployment Configuration
open `_config.yml` file under `blog` folder, search deploy

```
deploy:
  type: git
  repo: https://github.com/username/username.github.io  # use your own username
  branch: master
```

#### 4) Deploy
Now, we can deploy our blog, before deploy we'd clean the cache and make sure we generated static files.

```
#Cleans the cache file (db.json) and generated files (public).
hexo clean

#Generates static files.
hexo generate

#Deploys your website.
hexo deploy

```

Wait one minute and Visit [https://username.github.io](https://username.github.io), Your blog is here now! Done!!
