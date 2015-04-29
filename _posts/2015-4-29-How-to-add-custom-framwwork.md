---
layout: post
title: How to generate custom framework and add it to the existing project
---
### In framework project:

1. Open framework project and build.
2. Right click on *.framework and select 'Show in Finder'.
3. Copy framework package to your place to save.

### In project which needs to add the framework:

- Open Finder and drag the framework package to the project. Check Copy if 
- Or select your target, go to [Build Phases - Link Binary With Libraries] and click '+', choose 'Add Other...' and locate the framework package.
