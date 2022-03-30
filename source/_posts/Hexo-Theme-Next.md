---
title: Hexo Theme Next
date: 2020-04-29 10:36:01
categories: 
- Blog Setting
tags:
- Next Theme
- Blog
- Hexo
---
[NextT](https://theme-next.js.org/docs/getting-started/) is a high quality elegant Hexo theme. I used it in this Blog.

## 1 Install NextT

### 1) Install NextT

Download NextT files to ```theme```

```bash
# change to your hexo folder (it is blog in my case)
$ cd blog

# clone NextT from github
$ git clone https://github.com/next-theme/theme-next-docs
```
<!-- more -->

### 2) Set Hexo Theme to NextT
> Hint:
> * The ```_config.yml``` file in ```blog``` folder is called ```hexo-config.yml``` in my article.
>   After chage ```hexo-config.yml```, we need restart server  
> * The ```_config.yml``` file in ```theme``` folder is called ```next-config.yml```  in my article.
>   We don't need to restart server after chage ```next-config.yml```

Open ```hexo-config.yml```, find ```theme```, change it to ```next```

```yml
theme: next
```

Now, we installed NextT successfully.

Let us start server and check our blog in browse

```bash
#generate the static files (html, css, etc) for your website
hexo generate

#Starts a local server. By default, this is at http://localhost:4000/.
hexo server
```
We can see the new theme.

## 2. NextT Setting
> Those are changes I set in my blog

### 1) WebStie informations Setting
open ```hexo-config.yml```

```yml
# Site
title: Maoru's Blog
subtitle: 'Saty Hungry, Stay Foolish'
description: ''
keywords:
author: Maoru Tian
language: en
timezone: ''
```

### 2) Scheme Setting
open ```next-config.yml```, search Schemes

```yml
# Schemes
#scheme: Muse
#scheme: Mist
#scheme: Pisces
scheme: Gemini
```

### 3) Menu Setting

* open ```next-config.yml```, search menu

```yml
menu:
  home: / || fa fa-home
  # about: /about/ || fa fa-user
  tags: /tags/ || fa fa-tags
  categories: /categories/ || fa fa-th
  archives: /archives/ || fa fa-archive
  #schedule: /schedule/ || fa fa-calendar
  #sitemap: /sitemap.xml || fa fa-sitemap
  #commonweal: /404/ || fa fa-heartbeat
```
we have about, tags, categories menu items now, but we don't have markdown file associated to them.

* create new pages

```bash
hexo new page "about"
hexo new page "tags"
hexo new page "categories"
```

### 4) Search Function
A search function can help you manage your blog better.

1. install hexo-generator-searchdb

```bash
npm install hexo-generator-searchdb --save
```

2. add the flowing code to the end of ```hexo-config.yml```

```yml
search:
  path: search.json (json is better than xml)
  field: post
  format: html
```

3. open ```next-config.yml```, search local_search

```yml
# Local search
local_search:
  enable: true
```

### 5) Social Links
open ```next-config.yml```, search social

```bash
social:
  GitHub: https://github.com/maorutian || fab fa-github
  #E-Mail: mailto:yourname@gmail.com || fa fa-envelope
  #Weibo: https://weibo.com/yourname || fab fa-weibo
  #Google: https://plus.google.com/yourname || fab fa-google
  #Twitter: https://twitter.com/yourname || fab fa-twitter
  #FB Page: https://www.facebook.com/yourname || fab fa-facebook
  #StackOverflow: https://stackoverflow.com/yourname || fab fa-stack-overflow
  #YouTube: https://youtube.com/yourname || fab fa-youtube
  #Instagram: https://instagram.com/yourname || fab fa-instagram
  #Skype: skype:yourname?call|chat || fab fa-skype
```

### 6) Highlight Codebook

1. Go to `config.yml` in `Hexo`, delete `wrap` and `hljs`
```yml
highlight:
  enable: true
  line_number: false
  auto_detect: false
  tab_replace: ''
prismjs:
  enable: false
  preprocess: true
  line_number: true
  tab_replace: ''
```

2. Go to ```config.yml``` in `Next`
```yml
codeblock:
  # Code Highlight theme
  # All available themes: https://theme-next.js.org/highlight/
  theme:
    light: routeros
    dark: rainbow
  prism:
    light: prism
    dark: prism-dark
  # Add copy button on codeblock
  copy_button:
    enable: true
    # Available values: default | flat | mac
    style: mac
```

That is all features I used in my blog, If you find more exciting features, Please share to me

