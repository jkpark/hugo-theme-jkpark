---
title: Get Started
description: 
date: 2020-11-01T12:20:07+09:00
draft: false
weight: 1
image: "" # relative path of /static/images folder
tags: [hugo]
category: blog
enableToc: true
---

# Create a New Site

```
hugo new site demo
```

The above will create a new Hugo site in a folder named `demo`.

# Add Theme

```
cd demo
git init
git submodule add https://github.com/jkpark/hugo-theme-jkpark.git themes/jkpark
```

Take a look inside the `exampleSite` folder of this theme.
```
themes/jkpark/exampleSite
├── content  # some example contents for demo site.
├── data
    └── aboutme.yaml
└── config
    └── _default
        ├── config.toml
        ├── menus.toml
        └── parems.toml
```

## remove unnessasory defaults files and folders.

```
rm -rf archetypes
rm config.toml
```

## config folder
To use this theme, copy the `config` folder in the root folder of your hugo site.

```
cp -r themes/jkpark/exampleSite/config .
```

### change configures

open the `config.toml` file in the `config` folder.


## data folder

contents of `data/aboutme.yaml` is displayed at the first section of the [main page](/).


# Create first content

```
hugo new blog/my-first-post.md
```

# Start the Hugo server

```
hugo server
```

Navigate to your new site at http://localhost:1313/.