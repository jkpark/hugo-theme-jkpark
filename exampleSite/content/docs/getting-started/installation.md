---
title: Installation
description: 
date: 2020-12-02T20:09:19+09:00
draft: false
weight: 1
image: "" # relative path of /static/images folder
type: docs
---

# Create a New Site

```
hugo new site demo
```

The above will create a new Hugo site in a folder named `demo`.

# Install `jkpark` theme as git submodule

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

When you remove `archetypes` folder, hugo will searches for the layout to use for a given page.

More informations about lookup order, https://gohugo.io/templates/lookup-order/

## move config folder
To use this theme, copy the `config` folder in the root folder of your hugo site.

```
cp -r themes/jkpark/exampleSite/config .
```

# Create first content

```
hugo new blog/my-first-post.md
```

# Start the Hugo server

```
hugo server
```

Navigate to your new site at http://localhost:1313/.