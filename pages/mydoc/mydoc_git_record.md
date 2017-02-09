---
title: Record
tags: [getting_started, troubleshooting]
keywords:
summary: "Git record-related command"
sidebar: mydoc_sidebar
permalink: mydoc_git_record.html
folder: mydoc
---

## Git record-related command
* In Git, commit only respects changes that have been marked explicitly with add.

```
git commit [-a]
git push [romote]
git tag foo
```

* git add 명령으로 파일들을 커밋할 목록에 추가하면 git commit 명령으로 커밋(히스토리의 한단위)을 만든다.
  * git commit -a 옵션을 이용하면 바뀐 파일을 자동으로 추가할 수 있다.
* git push 명령으로 Github에 밀어 넣는다.
* git tag 명령으로 이미 만들어진 태그가 있는지 확인할 수 있다. 알파벳 순서로 태그를 보여준다.
