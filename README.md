# lowtech.io

Content for static site at [https://lowtech.io](https://lowtech.io)

## Building

Site content is built with [Hugo v0.100.1](https://github.com/gohugoio/hugo/releases/tag/v0.100.1) which typically needs to be manually installed as the releases move faster than most repos update.

## Adding a Library resource

### 1. File naming convention

**Naming convention**: ```YYYY-mm-dd-several-unique-identifying-words.md```

Simplest way is to duplicate an existing markdown file in ```/content/library``` (keep in
same directory) and rename it. The file name will be clean URL of the post.

**Note**: the date should be the date of publication of the resource, not the date of adding
the content to the Library.


### 2. File contents convention

File contents should reflect the title and the publication date of the resource.

The file header should contain:

```
---
title: "<title of the resource>"
date: <YYYY-mm-dd publication date of the resource, like "2022-06-06">
draft: false
tags:
- pages                    <----- Mandatory
- library                  <----- Mandatory
- add
- your
- own
- tags
---


<One or two short sentences that describe what the viewer will learn at the end>

----

<Title this section 'Content' or 'Video' or something similarly informative>
```

### 3. Shortcodes

Shortcodes assist in embedding common content, such as tweets, YouTube, Vimeo, etc. More
shortcodes are described on the [Hugo shortcodes documentation](https://gohugo.io/content-management/shortcodes/) page

Common shortcodes are:

#### Youtube

Take the URL of the video and in the *Content* section and insert the short code:
```
{{< youtube QBCX3Oxp3vw >}}
```

#### Twitter

E.g. if you have a tweet such as ```https://twitter.com/hiredbeard/status/1533363402160361472```

Take the User ID and the Tweet ID and in the *Content* section and insert the short code:
```
{{< tweet user="hiredbeard" id="1533363402160361472" >}}
```
