---
title: How to Create New Project
description: "explain how to create new project."
date: 2020-11-11T20:16:45+09:00
draft: false
weight: 0
image: "" # relative path of /static/images folder
tags: [hugo, project]
category: blog
enableToc: true
---

# Create Hew project

you can create new project directory using `--kind project-bundle`

```
archetypes
└── project-bundle
    ├── images
    │   └── preview.png
    └── index.md
```

```
$ hugo new --kind project-bundle projects/first-project
```

Will create a new project in `/content/projects/first-project` with the same set of files as in the `project-bundle` archetypes folder.

You can override `preview.png` to your preview image of project.

each project will be displayed at the project section of the [main page](/) and more contents at the [project page](/projects/first-project/)