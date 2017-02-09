---
title: git branch-related command
tags: [getting_started, troubleshooting]
keywords:
summary: "Writing git manual"
sidebar: mydoc_sidebar
permalink: mydoc_git_branch.html
folder: mydoc
---

# 브랜치
### 브랜치란 커밋 사이를 가볍게 이동할 수 있는 어떤 포인터 같은 것이다.

 최초로 커밋하면 Git은 master라는 이름의 브랜치를 만들어서 자동으로 가장 마지막 커밋을 가리키게 한다.
![Image of branch](https://git-scm.com/figures/18333fig0303-tn.png)

그림 1. 가장 최근 커밋 정보를 가리키는 브랜치

이해를 돕기 위해 testing 브랜치를 만든다.

```
$ git branch testing
```

위의 새로 만든 브랜치도 지금 작업하고 있던 마지막 커밋을 가리킨다.

![Image of testing branch](https://git-scm.com/figures/18333fig0304-tn.png)

그림 2. 커밋 개체를 가리키는 두 브랜치

Git은 Head라는 특수한 포인터로 지금 작업하는 로컬 브랜치를 가리킨다.
git branch 명령은 브랜치를 만들기만 하고 브랜치를 옮기지 않는다.
git checkout 명령으로 새로 만든 브랜치로 이동할 수 있다.

```
$ git checkout testing
```

![Image of head](https://git-scm.com/figures/18333fig0306-tn.png)

그림 3. HEAD는 옮겨간 다른 브랜치를 가리킨다.
