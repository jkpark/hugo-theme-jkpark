---
title: Hosting on GitHub Pages
description: 
date: 2020-12-02T20:09:19+09:00
draft: false
weight: 3
image: "" # relative path of /static/images folder
type: docs
---


# Create New Repository on the github

Go [github](https://github.com/) and create new public Repository.

# import your hugo folder into github

goto your hugo folder which we made from the previous post.

```
cd demo
```

```
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/<your repo>
git push -u origin main
```

now, hugo server is placed in the your github repo.

# Deployment of hugo server from github pages.

There are 2 types of GitHub Pages:

 - User/Organization Pages ( https://<USERNAME|ORGANIZATION>.github.io/ )
 - Project Pages (h ttps://<USERNAME|ORGANIZATION>.github.io/<PROJECT>/ )

## Deploying as User/Organization Pages


## Deploying as Project Pages

You can also tell GitHub pages to treat your main branch as the published site or point to a separate gh-pages branch. The latter approach is a bit more complex but has some advantages:

 - It keeps your source and generated website in different branches and therefore maintains version control history for both.
 - Unlike the preceding docs/ option, it uses the default public folder.

### gitignore public folder

First, add the public folder to your .gitignore file at the project root so that the directory is ignored on the main branch
```
echo "public" >> .gitignore
```

### init `gh-pages` branch

```
git checkout --orphan gh-pages
git reset --hard
git commit --allow-empty -m "Initializing gh-pages branch"
git push origin gh-pages
git checkout main
```

### Rebuild and Deployment

```
rm -rf public
git worktree add -B gh-pages public upstream/gh-pages
```

```
hugo
cd public && git add --all && git commit -m "Publishing to gh-pages" && cd ..
git push upstream gh-pages
```

### Set `gh-pages` as your publish branch

In order to use your gh-pages branch as your publishing branch, you’ll need to configure the repository within the GitHub UI. This will likely happen automatically once GitHub realizes you’ve created this branch. You can also set the branch manually from within your GitHub project:

1. Go to Settings → GitHub Pages
2. From Source, select “gh-pages branch” and then Save. If the option isn’t enabled, you likely have not created the branch yet OR you have not pushed the branch from your local machine to the hosted repository on GitHub.
After a short while, you’ll see the updated contents on your GitHub Pages site.
