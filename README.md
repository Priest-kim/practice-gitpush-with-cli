# CLI만 이용해서 github에 푸시하기

```bash

# 1. git init 생성하기
git init

# 2. 레파지토리로 설정한 폴더에 있는 파일 staging 하기
# add . <- 은 모든 변경 사항 올리기
# add <파일명> <- 특정 파일만 올리기
git add .


# 3. 커밋 메시지 작성하고 커밋하기
git commit -m "<메시지 작성>"

# 4. git repo 생성 및 push 하기
#  레파지토리 생성 및 모든 소스 한번에 푸시 하는 명령어
gh repo create <레파지토리명> --public --source=. --=remote=origin --push

# gh를 설치하지 않은 경우
# github에서 레파지토리 생성 후 url 복사
git remote add origin <레파지토리 url>

```
# 주요 Git CLI 명령어
---
## 🔧 초기 설정 관련
- git config --global user.name "이름" : 사용자 이름 설정
- git config --global user.email "이메일" : 사용자 이메일 설정
- git config --list : 설정 확인

## 🗂️ 저장소 관리
- git init : 현재 디렉토리를 Git 저장소로 초기화

## 📝 변경 사항 추적
- git status : 현재 작업 상태 확인 (변경 파일 등)
- git add <파일> : 변경 파일을 스테이지 영역에 추가
- git add . : 모든 변경 파일을 스테이지에 추가
- git commit -m "커밋 메시지" : 스테이지에 있는 변경사항 커밋
※ git commit : 커밋 메시지 입력창이 자동으로 뜸. 입력 후 저장하고 닫으면 됨

## 🔄 버전 이동 & 기록 보기
- git log : 커밋 로그 보기
- git log --oneline : 한 줄 요약 로그 보기
- git checkout <브랜치명> : 다른 브랜치로 전환

## 🌿 브랜치
- git branch : 현재 브랜치 목록 확인
- git branch <이름> : 새 브랜치 생성
- git checkout -b <이름> : 브랜치 생성 + 이동
- git merge <브랜치> : 현재 브랜치에 다른 브랜치 병합
- git branch -D <이름> : 브랜치 삭제

## ☁️ 원격 저장소
※ 원격 저장소에 업로드하기 전 반드시 github에 접속하여 새 repository 생성해야 함

- git remote add origin <repository 주소> : 현재 프로젝트를 원격 저장소와 연결
- git remote -v : 원격 저장소 목록 확인
- git push origin <브랜치> : 원격 저장소의 특정 브랜치에 업로드
