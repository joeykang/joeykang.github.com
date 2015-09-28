---
layout: post
title: How to sync/backup directory with rsync on OSX
---
### In Shell:

	rsync -avE --delete <source object> <dest dir>

Notes: `source object` will be synchronized in `dest dir`.

-a: keep source date  
-v: verbose  
-E: Apple specific option  to  copy  extended  attributes,  resource forks,  and  ACLs.   Requires at least Mac OS X 10.4 or suitably patched rsync.  
--delete: delete files in <dest dir> that don't exist in <source dir>

Other options:
--exclude=pattern_to_exclude

### Windows 7:
	robocopy <Source dir> <Dest dir> /e /mir /np /log:backup_log.txt
