---
author: Christian Blunden
comments: true
date: 2012-05-21 07:25:00+00:00
layout: post
slug: cloning-git-repo-into-existing-folder
title: Cloning git repo into existing folder
wordpress_id: 132365457
---

In the git help pages it says

<directory> The name of a new directory to clone into. The "humanish" part of the source repository is used if no directory is explicitly given (repo for /path/to/repo.git and foo for host.xz:foo/.git). Cloning into an existing directory is only allowed if the directory is empty.

So if you do need to do this, then a work around is:

Clone the repository without checking out the contents to a new folder

`git clone -n <repo>`

Then move the git folder to where it needs to be

`mv .git <existing folder>`

Then force a check out the contents

`git checkout -f master`

_Warning: This come with no guarantee of success. Works on my machine..._
