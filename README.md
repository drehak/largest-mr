# Attempt at the largest MR diff number possible: +82,556,506 lines

**In short: [+82,556,506](https://github.com/drehak/largest-mr/pull/3) seems to work, while [+82,556,507](https://github.com/drehak/largest-mr/pull/4) does not.**

---

Made more or less by semi-manually force-pushing over and over and bisecting the number. All of the added lines are empty. I don't know where this number comes from. One of the thresholds I expected was above 50 MiB (so +52,428,801 or more), as that's when GitHub started to show a warning on push:

```
remote: warning: See https://gh.io/lfs for more information.
remote: warning: File f is 78.73 MB; this is larger than GitHub's recommended maximum file size of 50.00 MB
remote: warning: GH001: Large files detected. You may want to try Git Large File Storage - https://git-lfs.github.com.
```

This, however, doesn't seem to affect whether the number shows or not.

As for other techniques I tried, I shortened file names, branch names and commiter email + name as much as possible (hence the single letters everywhere). Despite `git --format-patch @~` producing a smaller file, this doesn't seem to matter here. Ironically, my first attempt without shortening everything got me to [+82,556,507](https://github.com/drehak/largest-mr/pull/1), but it doesn't show anymore and I failed to reach it again. It is what it is.
