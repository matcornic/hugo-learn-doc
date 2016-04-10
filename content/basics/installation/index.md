---
title: Getting started
prev: /basics/requirements
next: /basics/configuration
weight: 15
toc: true
---

The following steps are here to help you initialize your new website. If you don't know Hugo at all, we strongly suggest you to train by following this [great documentation for beginners](https://gohugo.io/overview/quickstart/).

## Create your project

Hugo provides a `new` command to create a new website.

```
hugo new site <new_project>
```

## Install the theme

Install the **Hugo-theme-learn** theme by following [this documentation](https://gohugo.io/themes/installing/)

The theme's repository is: https://github.com/matcornic/hugo-theme-learn.git

## Basic configuration

When building the website, you can set a theme by using `--theme` option. We suggest you to edit your configuration file and set the theme by default. Example with `config.toml` format.

```toml
theme = "hugo-theme-learn"
```

## Create your first chapter page

**Hugo-theme-learn** provides archetypes to create skeletons for your website. Begin by creating your first chapter page with the following command

```
hugo new --kind chapter basics/index.md
```

## Create your first content pages

Then, create content pages inside the previous chapter. Here are two ways to create content in the chapter :

```
hugo new basics/first-content.md
hugo new basics/second-content/index.md
```

## Launching the website

Launch the following command

```
hugo serve
```

Go to `http://localhost:1313/basics`

If you are curious, at the home page (http://localhost:1313/), you should see an empty homepage. It's because this theme does not really provide a default homepage.

You typically have 2 choices :

1. Create an [overview homepage](https://gohugo.io/templates/homepage/) for your project. Write an `index.html` file in *layouts/* folder.
2. Create a redirection to one your documentation page. Either by:
  1. Configuring your server to automatically redirect homepage to one your documentation page - *Recommended*
  2. Creating an empty html page with the following code in the head tag :  

  ```html
  <meta http-equiv="refresh" content="0; url=http://example.com/"/>
  ```
