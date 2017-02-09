---
title: Publish
tags: [getting_started, troubleshooting]
keywords:
summary: "Writing git manual"
sidebar: mydoc_sidebar
permalink: mydoc_git_publish.html
folder: mydoc
---

# GIT Publish-related command


Publish는 변경 내용을 발행하는 것이다. 현재의 변경내용은 아직 로컬 저장소의 head 안에 있다. 프로젝트를 공유하고 싶을 때 리모트 저장소에 Push할 수 있다. 이 명령은 git push [리모트 저장소 이름] [브랜치 이름]로 단순하다. master 브랜치를 origin 서버에 Push하려면 아래와 같이 서버에 Push한다.


### - publish의 명령어 
```
$ git push
$ git push remote
$ git format-patch origin
```


### $ git push
이 명령은 Clone한 리모트 저장소에 쓰기 권한이 있고, Clone하고 난 이후 아무도 리모트 저장소에 Push하지 않았을 때만 사용할 수 있다. 다시 말해서 Clone한 사람이 여러 명 있을 때, 다른 사람이 Push한 후에 Push하려고 하면 Push할 수 없다. 먼저 다른 사람이 작업한 것을 가져와서 머지한 후에 Push할 수 있다. 

### $ git format-patch origin
이 명령은 소스코드가 동일하지만 둘 이상의 브랜치에 적용해야 하는 경우 한 곳에서 작업한 내용을 다른 곳에 쉽게 반영하려면 먼저 방금 커밋한 내용에 대한 패치 파일을 생성한다.
