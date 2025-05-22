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
