# Git

## 1. Git 프로그램 설치

- 다운로드(https://git-scm.com/)

- 64-bit Git for Windows Setup 설치

## 2. Git 버전 확인

- 키보드 윈도우 + 키보드 R : `cmd` 입력

```bash
git --version
```

- 출력창 확인

## 3. VSCode에 Git 설정

#### 3-1. 터미널 환경을 git bash로 설정

- 윈도우, 맥, 리눅스의 명령창을 통일하기 위함

- 관리도구 클릭 > 설정메뉴 선택 > `dafault:Windows` 검색 > `Git Bash` 선택 > 재실행

#### 3-2. VSCode에서 Git 옵션 설정

- 터미널 실행 : `Ctrl + 백틱`

- git 버전 확인

```bash
git --version
```

- 기본 브랜치명 `main`으로 설정

```bash
git config --global init.defaultBranch main
```

- 윈도우, 맥, 리눅스 환경에서 Enter키 처리를 통일

```bash
git config --global core.autocrlf true
```

- git commit 명령을 VSCode에서 작성하도록 설정

```bash
git config --global core.editor "code --wait"
```

- git 사용자 아이디 설정

```bash
git config --global user.name "아이디"
```

git 사용자 아이디 확인

```bash
git config --global user.name
```

- git 사용자 이메일 저장

```bash
git config --global user.email "이메일"
```

- git 사용자 이메일 확인

```bash
git config --global user.email
```

## 4. Git 작업(실습)

#### 4-1. Git 프로젝트 관리 초기화

```bash
git init
```

#### 4-2. Git 현재 상태 파악

```bash
git status
```

#### 4-3. Git 현재 수정된 내용, 파일, 폴더 등 저장

- 원하는 파일만 저장

```bash
git add README.md
```

- 모든 파일 및 폴더 저장(추천)

```bash
git add .
```

#### 4-4. 수정 내역 메모

- 한줄 작업 메모

```bash
git commit -m "작업 관련 설명글 작성"
```

- 여러줄 작업 메모(제목, 상세내용)

```bash
git commit
```

#### 4-5. commit 내용 컨벤션

```bash
[커밋타입] : 커밋메세지(옵션)
```

- 커밋 타입 : 작업의 분류

- 옵션 : 이슈 또는 수정이 된 작업 커밋 번호 또는 추가정보

- 커밋 메세지 : 무엇을 했는지 짧은 내용

##### 4-5.1 커밋 타입

- `[feat]` : 새로운 기능 추가

- `[fix]` : 버그 수정

- `[docs]` : 문서 수정(README.md)

- `[style]` : 코드의 스타일 변경(띄워쓰기, 세미콜론 등)

- `[refector]` : 코드 리팩토링(기능 변경, 코드 정리 등)

- `[test]` : 테스트 코드 추가

- `[chore]` : 기타(빌드 설정, 패키지 업데이트 등)

##### 4-5.2 옵션

- 만약 `회원가입 로그인 기능 추가`라면

- 아래는 이슈 #23을 해결하고 기능을 추가

```
[feat]:회원가입 로그인 기능 추가(#23)
```

##### 4-5.3 커밋 내용

- Enter키 기준으로 제목과 내용 구분

```
[docs] : 커밋 제목

커밋 상세 내용 작성
```

#### 4-6. 커밋 내용 확인

- 기존의 commit된 내용을 확인

- 상세보기

```bash
git log
```

- 간략하게 보기

```bash
git log --oneline
```

- 하나의 commit 상세보기

```bash
git show 커밋아이디
```

##### 4-6.1 각 항목 관련 사항 이해

- commit : 고유한 커밋 번호(아이디)

- Author : 작성자

- Date : 날짜

- message : 상세내용

#### 4-7. 브랜치 작업해보기

- `나뭇가지`라는 의미로 원 줄기로부터 파생되는 것을 말함

- 원 `소스`로부터 파생된 새롭게 `분기한 소스`관리를 말함

- 브랜치 생성시에는 add와 commit이 완료되어야함

##### 4-7.1 브랜치 생성

```bash
git add .
git commit -m "[docs]:브랜치 실습 test 생성하기"
git branch test
```

##### 4-7.2 브랜치 목록 확인

```bash
git branch -v
```

##### 4-7.3 브랜치 이동

```bash
git switch test
```

##### 4-7.4 브랜치 삭제

```bash
git branch -D test
git branch -v
```

##### 4-7.5 브랜치 병합(가급적 사용 X)

- 브랜치 하나로 병합

- 주의 사항 : main 브랜치에서 test 브랜치를 합침

```bash
git merge 합치고자 하는 브랜치명
```

#### 4-8. git 브랜치 충돌 해결

- 추후 GitHub협업에서 자세히 알아봄

# GitHub

## 1. GitHub 회원가입

- http://github.com

## 2. GitHub 프로젝트(Repository) 생성

- 만약 til_git 프로젝트를 생성했다면 GitHub에도 동일하게 생성

  - public으로 세팅(외부로 소스 공개)

  - description 작성(프로젝트 설명)

## 3. GitHub 인증

#### 3-1. 무조건 GitHub에 로그인 된 상태로 시도

#### 3-2. `윈도우 > 자격 증명 관리자 > Windows 자격 증명` 에서 GitHub 확인

- 새로 생성하길 권장

- PC 정리 또는 자리 이동시 반드시 삭제

## 4. GitHub에 프로젝트 연결

#### 4-1. 원격 저장소 주소 지정

- `remote`는 원격(인터넷)을 말함

- `add`는 추가하라는 뜻

- `origin`은 원격이름. http 주소에 간략하게 별칭을 주는 것(단어는 마음대로 가능)

```bash
git remote add origin https://github.com/aspynlyn/til_git.git
```

#### 4-2. 원격 저장소 목록 보기

```bash
git remote -v
```

#### 4-3. 원격 저장소에 소스 등록

- 습관처럼 하면 좋은 작업(Ctrl + S 후)

```bash
git add .
git commit -m "[docs]:최초등록"
```

- 소스 업로드를 `push` 한다고 말함

```bash
git push -u origin main
```

```bash
git push origin main
```

- `-u`옵션을 붙였다면 이후로는 `git push`만 적으면 됨

#### 4-3. 원격 저장소 관리

- 목록 보기

```bash
git remote -v
```

- 삭제 하기

```bash
git remote remove 원격이름
```

- 추가하기

```bash
git remote add 원격이름 https주소
```

- 이름 바꾸기

```bash
git remote rename 기존이름 바꿀이름
```

#### 4-5. 추천 작업 순서

```bash
git add .
git commit -m "[docs]:git 학습"
git push origin main
```

## 5. GitHub의 소스를 복사(Clone)해서 작업하는 법

- GitHub 주소를 주의해야함
  - 코드 소스 기준 `http`로 진행
  - 코드 소스 기준이 `ssh`면 인증을 다시 처리하는 과정 필요

#### 5-1. 실습

- 서울로 출장을 감(PC도 없이) 서울 사무소에서 PC를 지급받은 상황

  - PC에 환경 설정 진행(VSCode, Git)

  - `D:/student/test 폴더` 생성

  - GitHub 사이트에 프로젝트를 `clone`함

  - GitBub 사이트에 Repository를 `clone`함

#### 5-2. clone

```bash
git clone 깃허브주소(https) .
```

#### 5-3. clone 이후의 작업

```bash
git status
git branch -v
git branch 새브랜치명
git switch 새브랜치명
작업진행
git add .
git commit -m "작업내용"
git push origin 새브랜치명
```

ㅇㅇㅇㅇㅇㅇㅇ00000000000
