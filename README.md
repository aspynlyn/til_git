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

##### 4-5.1. 커밋 타입

- `[feat]` : 새로운 기능 추가

- `[fix]` : 버그 수정

- `[docs]` : 문서 수정(README.md)

- `[style]` : 코드의 스타일 변경(띄워쓰기, 세미콜론 등)

- `[refector]` : 코드 리팩토링(기능 변경, 코드 정리 등)

- `[test]` : 테스트 코드 추가

- `[chore]` : 기타(빌드 설정, 패키지 업데이트 등)

##### 4-5.2. 옵션

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

#### 4-6 커밋 내용 확인

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

- message : 
# GitHub