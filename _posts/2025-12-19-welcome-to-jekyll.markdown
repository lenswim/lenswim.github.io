---
layout: post
title:  "Github Pages with Jekyll"
date:   2025-12-19 15:25:31 +0100
categories: github-pages jekyll
---
# Github pages with Jekyll
[github pages documentation](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)

## Installing Jekyll
[Jekyll install guide](https://jekyllrb.com/docs/installation/)
1. install ruby (sudo apt install ruby)
2. install ruby gems (already installed, maybe by step 1. who knows?)
3. install GCC (The GNU Compiler Collection (GCC) is a comprehensive suite of free software compilers, already installed)
4. install make (command-line utility used for build automation, primarily on Unix-like systems, already installed)
5. [install Jekyll for Ubuntu](https://jekyllrb.com/docs/installation/ubuntu/)

no idea if it worked but it said some things like:
```
Installing ri documentation for jekyll-4.4.1
Done installing documentation for unicode-display_width, terminal-table, safe_yaml, rouge, forwardable-extended, pathutil, mercenary, liquid, rexml, kramdown, kramdown-parser-gfm, ffi, rb-inotify, rb-fsevent, listen, jekyll-watch, google-protobuf, sass-embedded, jekyll-sass-converter, concurrent-ruby, i18n, http_parser.rb, eventmachine, em-websocket, colorator, base64, public_suffix, addressable, jekyll after 25 seconds
Fetching bundler-4.0.2.gem
Successfully installed bundler-4.0.2
Parsing documentation for bundler-4.0.2
Installing ri documentation for bundler-4.0.2
Done installing documentation for bundler after 0 seconds
30 gems installed
```

## Create new github repo
lenswim/lenswim.github.io

do stuff on the pages section, but I need to have content in my repo

commit & push this file

To create a new Jekyll site, use the jekyll new command in your repository's root directory:

```
jekyll new --skip-bundle .
```

Creates a Jekyll site in the current directory

```
Conflict: /home/wim/projects/Learnings/github-pages/lenswim.github.io exists and is not empty.
                    Ensure /home/wim/projects/Learnings/github-pages/lenswim.github.io is empty or else try again with `--force` to proceed and overwrite any files.

```

yo, lame


```
jekyll new --skip-bundle .
```

ok, this worked

following guide and uncomment the github line in gemfile

```
bundle install
```
```
Fetching gem metadata from https://rubygems.org/..........
Resolving dependencies...
Could not find compatible versions

Because github-pages >= 232 depends on jekyll = 3.10.0
  and Gemfile depends on jekyll ~> 4.4.1,
  github-pages >= 232 cannot be used.
So, because Gemfile depends on github-pages ~> 232,
  version solving has failed.
```

okay, maybe read the doc better, because it clearly said I also need to check this page here for [supported versions](https://pages.github.com/versions.json)

okay, updated gemfile again and it worked this time.

### Running your site locally

```
bundle exec jekyll serve
```


yaay, it works
