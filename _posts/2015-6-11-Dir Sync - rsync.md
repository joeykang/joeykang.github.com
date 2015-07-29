---
layout: post
title: How to sync/backup directory on OSX
---
### In Shell:

	rsync -aE --delete <source dir> <dest dir>

-- delete: delete files in <dest dir> that don't exist in <source dir>

Note: Exceptions happen sometimes


