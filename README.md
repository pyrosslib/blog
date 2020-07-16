# PyRoss blogging guide

You can visit the site at: https://pyrosslib.github.io/

## How to upload a new notebook post

Add your notebook to the `_notebooks` directory in the repository, commit and make a pull request. The name of the file should always be prefaced with the upload date (e.g. `2020-02-20-notebook-title.ipynb`).

The first cell of the notebook should always be of this form:

```
# Notebook title
> Notebook description

- toc: true 
- badges: true
- comments: true
- categories: [notebook, simulation, testing]
```

- If `toc` is set to true, then a table of contents will be generated for the post.

- If `badges` is set to true, then GitHub, Colab and Binder badges will be displayed on the post. To hide a specific badge, use `hide_{github,colab,binder}_badge: true`.

- You can put the notebook into specific categories using the `categories` field.

- If `comments` is set to true, then a comment section is added to the post.

- To set an image for the notebook use
  ```
  - image: images/img.png
  ```
  and place your image in the `blog/_notebooks/images` directory.

See [this](https://github.com/fastai/fastpages#writing-blog-posts-with-jupyter) for more information on how to customize your post.

## How to upload a new Markdown post

Add a Markdown file to the `_posts` directory, commit and make a pull request. The name of the file should always be prefaced with the upload date (e.g. `2020-02-20-post-title.md`).

Include the following in the top of your file, and edit the `title`, `description` and `categories`.

```
---
toc: true
layout: post
title: Post title
comments: true
description: Post description
categories: [news]
---
```

See [this](https://github.com/fastai/fastpages#writing-blog-posts-with-markdown) for more information on how to customize your post.
