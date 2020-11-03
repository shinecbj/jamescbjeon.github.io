---
layout: post
title: Git CLI Backup
subtitle: 생활코딩 Git CLI Backup 정리노트
categories: markdown
tags: [Git, CLI, Backup, 생활코딩, 정리노트]
---

*본 포스트는 필수 개발 도구인 Git의 백업(Backup)에 대한 정리노트입니다.*

*포스트 내 모든 내용은 [생활코딩 - Git CLI - Branch & Conflict 수업][git-cli-branch]에 기반하고 있습니다. 해당 내용 수강 후 아래 내용으로 정리노트로 사용하시길 권장합니다.*

> 생활코딩 Git CLI 정리노트   
  1. [Version - 버전관리][git1]
  1. [Branch & Conflict - 가지 및 충돌][git2]
  1. [Back-up - 백업][git3]
  1. [Collaboration - 협업][git4]
  1. ~~Cherry pick & rebase~~
  1. ~~Github pull request~~

[git1]: https://jamescbjeon.github.io/markdown/2020/10/29/opent-git-cli-version.html
[git2]: https://jamescbjeon.github.io/markdown/2020/10/30/opent-git-cli-branch.html
[git3]: https://jamescbjeon.github.io/markdown/2020/10/31/opent-git-cli-backup.html
[git4]: https://jamescbjeon.github.io/markdown/2020/11/01/opent-git-cli-collaboration.html
[git-cli-branch]: https://opentutorials.org/course/3841

***

## 0 커버페이지

## 수업의 목표와 용어정리

Local repository --> Remote repository
		push

Remote repository --> Local repository #2
		clone

Remote --> Local
	pull

git hosting	원격 저장소를 임대해주는 것

## Git hosting

(git hosting 검색) 비교해 볼 것
	--> github, gitlab

## 공부의 방향

	Local to remote		Remote to local

HTTP

SSH


HTTP --> 보안적으로는 다소 취약. 배울 필요 없음.
SSH --> 보안성 높음. 배우기 어렵고, 다소 난해

## 원격저장소와 연결

## git push

git push	local - remote가 이미 연결되어 있으면 바로 실시

에러 발생 --> 'git push --set -upstream origin master'
	어떤 remote repo에 연결할 건지 문의
	해당 명령어대로 입력 후 재실행
		github id/pw 입력

(실습)
nano hello1.txt
	마지막에 backup 저장
git status
git add hello1.txt
git commit -am "backup"
git push
	id/pw

## git pull

(실습)
pwd
	Dcouments/git/...
git
Github - 'Clone or download (초록버튼)' - HTTPS link copy
git clone 주소 (원하는 디렉토리 이름/생략가능)
해당 디렉토리에 저장소이름대로 디렉토리 생성 후 저장

## git pull

git remote -v	어떤 원격저장소에 연결되었는지 확인

git pull	연결된 remote에서 자동으로 당겨옴
git log

작업순서	pull --> 작업 --> add --> commit --> push

## git과 오픈소스

## 수업을 마치며
추가로 공부하면 좋은 주제

SSH	저장소 간 통신 방법 - 자동으로 로그인 가능
github/gitlab	기능을 꼼꼼히 살펴보자
	ex. issue tracker
협업	conflict - 충돌을 어떻게 해결할 것인가
	충돌방지에 대해 공부
