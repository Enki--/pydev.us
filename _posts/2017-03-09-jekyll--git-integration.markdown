---
title: Jekyll & Git Integration
layout: post
---

Set up is really stolen from [here](https://www.mikekasberg.com/software%20development/2016/11/08/automated-jekyll-deployments.html).

Breaks down to running the below code via cron once an hour

> GIT_REPO=$HOME/myjekyllsite.git
> TMP_GIT_CLONE=$HOME/tmp/myjekyllsite
> PUBLIC_WWW=$HOME/mypodcast.com

> # Check out the Git repository so we have a working copy in a temp dir.
> git clone $GIT_REPO $TMP_GIT_CLONE

> # Build it.
> jekyll build -s $TMP_GIT_CLONE -d $TMP_GIT_CLONE/_site

> # Deploy it.
> cp -r $TMP_GIT_CLONE/_site/* $PUBLIC_WWW

> # Clean up.
> rm -rf $TMP_GIT_CLONE

> echo "Done."
> exit