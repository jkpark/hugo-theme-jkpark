---
title: {{ replace .Name "-" " " | title }}
description: 
date: {{ .Date }}
draft: false
weight: 0
image: "" # relative path of /static/images folder
type: docs
---

recommand to create new `doc` type markdown with:

```
hugo new --kind doc docs/doc-name
```