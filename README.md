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
# GitHub