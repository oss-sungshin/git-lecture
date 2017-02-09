---
title: Create
tags: [getting_started, troubleshooting]
keywords:
summary: "Writing git manual"
sidebar: mydoc_sidebar
permalink: mydoc_git_create.html
folder: mydoc
---


## Create

```
From existing files
   git init
   git add .
   git commit

From remote repository
   git clone .../old .../new
   git clone git://...
   git clone ssh://...
```
<<<<<<< HEAD
=======

## Writing git manual! 
Writing git manual! 
>>>>>>> 30fed7edd625cb4639f71c0345d7b8cdcd99686c


 * git init


이 명령은 .git이라는 하위 디렉토리를 만든다.


.git 디렉토리에는 저장소에 필요한 뼈대 파일(Skeleton)이 들어 있다.


*  git add .

Git이 파일을 관리하게 하려면 저장소에 파일을 추가하고 커밋해야 한다.

git add 명령으로 파일을 추가하고 커밋한다:

*  git commit


Git은 생성하거나 수정하고 나서 git add 명령으로 추가하지 않은 파일은 커밋하지 않는다.

그 파일은 여전히 Modified 상태로 남아 있다.

커밋하기 전에 git status 명령으로 모든 것이 Staged 상태인지 확인할 수 있다. 그리고 git commit을 실행하여 커밋한다:

*  git clone


github에서 소스를 최초로 내려받을때, git clone명령어를 사용하면 된다.

이는 저장소를 복제한다는 뜻이다.
