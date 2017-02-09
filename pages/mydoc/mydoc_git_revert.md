---
title: git revert-related command
tags: [getting_started, troubleshooting]
keywords:
summary: "Writing git manual"
sidebar: mydoc_sidebar
permalink: mydoc_git_revert.html
folder: mydoc
---

# 되돌리기

## 1. add를 잘못한 경우

stage 영역에 추가하고 싶지 않은 파일을 잘못 추가했다면 git reset을 이용한다.
```
$ git reset 파일이름
```

## 2. commit을 잘못한 경우
다시 커밋하고 싶으면 --amend 옵션을 사용한다.

```
$ git commit --amend
```

이는 이전 commit을 현재 stage영역의 상태로 덮어쓴다. 따라서 방금 한 commit을 다시 하고 싶으면, 파일을 수정한 뒤 add로 stage에 올리고 commit --amend를 해주면 된다.

amend 외에도 revert 명령어를 이용할 수 있다.

```
$ git revert HEAD
```

![Image of revert](http://img1.daumcdn.net/thumb/R1920x0/?fname=http%3A%2F%2Fcfile7.uf.tistory.com%2Fimage%2F2416ED455802179106E51A)

commit --amend와 다른점은 revert는 commit을 삭제한 이력을 다른 commit으로 남긴다는 점이다.	
이미 push를 했다면 amend나 reset을 사용하기 어렵기 때문에 revert를 해야할 수 밖에 없는 상황도 있다. 만약 하나 이상의 commit을 revert하고 싶다면 merge하는 것과 비슷하게 conflict를 해결해줘야한다. 

## 3. commit을 많이 잘못했다 or 수정을 하기 전으로 되돌리고 싶다.

어디서부터 잘못했는지 모르겠다. 적어도 내가 아는데부터 다시 시작하고 싶다. 또는 수정사항을 만들기 전으로 복원시키고 싶다.
이 경우에는 git reset의 다른 형태를 사용하면 된다.

```
$ git reset [option] commitId
```

reset은 사용자의 저장소와 작업 디렉토리를 특정 시점 상태로 변경한다.	
메카니즘을 들여다보면 HEAD 참조를 지정된 commit 시점으로 변경한 후, 인덱스를 변경하여 해당 commit을 반영한다.	
옵션에 따라 HEAD, 인덱스 뿐만아니라 작업 디렉토리 내의 모든 파일이 변경될 수 있기때문에 반드시 주의하여 사용하여야 한다.

##### 주요 옵션

 * --soft

	git reset --soft [commit id]
--soft 옵션은 지정된 commit을 가리키도록 HEAD 참조를 변경한다. 인덱스와 작업 디렉토리의 내용은 그대로 유지된다.
이 옵션은 새 커밋을 가리키도록 심볼릭 참조의 상태만을 변경한다.

 * --mixed
 
	git reset --mixed [commit id]
--mixed 옵션은 지정된 commit을 가리키도록 HEAD를 변경한다. 따라서 commit에 맞게 인덱스의 내용도 변경된다.
reset의 기본옵션이다.

 * --hard

	git reset --hard [commit id]
--hard 옵션은 HEAD, 인덱스 뿐만아니라 작업 디렉토리까지 commit과 같은 상태로 변경한다.
굉장히 위험한 옵션이니 사용시 주의가 필요하다.


따라서 다 지우고 다시 시작하고 싶은 때는 hard를 옵션으로 주면 된다. 이를 이용해 잘못 수정한 파일들을 HEAD 상태로 다시 복원할 수 있다.

```
$ git reset --hard HEAD
```

출처: http://llnntms.tistory.com/5 [IGNITER]
출처: http://donggov.tistory.com/29 [동고랩]