# Jekyll notes

## New Jekyll project
`jekyll new <site name>`

## Serve your website locally
`bundle exec jekyll serve`
* access website at localhost:4000


## The _site folder
this is the folder containing your built website


## Online notes
[Structuring posts](https://miklb.com/blog/2016/04/26/organizing-jekyll-posts/)

> you can create top level folders each with their own _posts sub-folder and Jekyll will read from each one, appending that folder name to the generated url for the post, i.e. a folder foo with _posts with 2016-04-26-post-title would yield a URL of example.com/foo/post-title (varying by your permalink structure). Those top level folders are then treated as categories, allowing for more filtration within your templates and site organization.


[Structuring - GH repo](https://github.com/yafred/organizing-posts-with-jekyll/blob/master/_config.yml)




## Pages vs Posts
a **page** is something like *localhost/about/*. It gives information. For example I could have them as indexes, such as: */who we are/*, *what we do*, *ansible tower*
a **post** on the other hand is a file that contains the actual information. Such us: *ansible-tower-backups.md*


## Organizing Blog posts based on categories only

```
---
layout: post
date: 2018-02-13
categories: ansible-tower devops #cat1, cat2, cat3 .....
permalink: /:categories
---
```

now I will have: /ansible-tower/devops

## Organizing Blog posts based on categories and title name
```
---
layout: post
title: ansible smells
date: 2018-02-13
categories: ansible-tower devops #cat1, cat2, cat3 .....
permalink: /:categories/:title.html
---
```
now I will have: /ansible-tower/devops/ansible-smells.html


## Nameing conventions and Post discovery
Jekyll is pretty annoying and it asks to follow specific nameing conventions for post discovery
1. Put all your posts in the **_posts** directory
2. you can create subfolders but always name your post: YYYY-MM-DD-<name>.md
3. Use permalinks to impose the URL to use.

```
|-- _posts
|   |-- 2018-09-16-first-article.markdown
|   |-- 2018-09-16-welcome-to-jekyll.markdown
|   `-- ansible-tower
|       `-- 2018-09-14-ansible-tower-intro.md
```

## Use Themes
1. Check online for the theme you like
2. update the Gemfile with something like: **gem "hanuman"**
3. run **bundle install**
4. Update **_config.yml** file. Like: **theme: hanuman**
**NOTE:** Most likely the new team will not have the *post* and *page* layout. It means that I will need to change my pages to adapt accordingly
Info and provided layouts can be found in the **layout** folder in the source GitHub repo for the theme



## Publish on GitHub
1. Create repo with no README.md
2. Update *baseurl* variable in the **_config.yml**
3. Create git repo: git init
4. Checkout gh-pages: git checkout -b gh-pages


## LunrJS
http://rayhightower.com/blog/2016/01/04/how-to-make-lunrjs-jekyll-work-together/
