---
title: git track-related command
tags: [getting_started, troubleshooting]
keywords:
summary: "Writing git manual"
sidebar: mydoc_sidebar
permalink: mydoc_git_track_files.html
folder: mydoc
---

![IMG1](images/img.JPG)

* 작업폴더의 파일을 깃이 추적하게 하거나 커밋을 위한 준비상태로 만드는 명령어
	* git add files
	* git add .
	* git add -i  (git 대화모드로 파일 staging)

* 파일명 수정
	* git mv old_name new_name

* 파일 또는 폴더를 삭제
	* git rm files

* 깃의 추적 중단시키기 (파일은 남기고 깃디렉토리에서만 삭제)
	* git rm --cached files
	
	