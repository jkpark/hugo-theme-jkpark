---
title: Project
description: 
date: 2020-12-02T20:09:19+09:00
draft: false
weight: 0
image: "" # relative path of /static/images folder
collapse: hide # show | hide | always
type: docs
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