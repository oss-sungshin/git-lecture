---
title: git resolve-related command
tags: [getting_started, troubleshooting]
keywords:
summary: "Writing git manual"
sidebar: mydoc_sidebar
permalink: mydoc_git_resolve_conflict.html
folder: mydoc
---

# Reslove Conflicts
##### Use add to mark files as resolved.
```
git diff [--base]
git diff --ours
git diff --theirs
git log --merge
gitk --merge
```

 * git diff는 두 커밋간이나 HEAD와 워킹 디렉토리의 차이점을 보여주는 명령어이다.
 * git diff 명령어를 사용하면 수정된 라인의 전, 후를 비교할 수 있다.
