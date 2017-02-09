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
### Use add to mark files as resolved.
예시는 아래와 같다.

```
git diff [--base]

git diff --ours

git diff --theirs

git log --merge

gitk --merge
```

 * git diff는 두 커밋간이나 HEAD와 워킹 디렉토리의 차이점을 보여주는 명령어이다.
 * git diff 명령어를 사용하면 수정된 라인의 전, 후를 비교할 수 있다.
 * git diff 명령어는 수정사항이 있을 때 많이 사용한다.
 * git diff <HEAD...원하는커밋아이디>를 써주면 처음부터 커밋아이디까지의 변경사항을 볼 수 있다.
