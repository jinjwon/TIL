# _Git (opens new window)_

![pont](https://velog.velcdn.com/images/dnrwhddk1/post/1c4d727f-25b3-44dc-aa82-f12996688782/image.png)

- git은 리누스 토발즈Linus Torvalds가 2005년에 만든 분산 버전 관리 시스템(DVCS)Distributed version control systems입니다. 수많은 회사에서 수많은 소스가 Git으로 관리되고 개발자라면 반드시 알아야 하는 기술 중 하나입니다.

- **Git의 특징**
- Git의 기본 기능은 이력 관리입니다. 많은 프로그램이 Ctrl + Z (undo)와 Ctrl + Y (redo)를 제공하는데, Git은 전체 소스 파일을 대상으로 해당 기능을 제공하고, 협업에 필요한 다양한 기능을 가지고 있습니다.

속성 용어 설명

- Git에서 사용하는 다양한 용어는 하나하나 실습하면서 소개할 예정이지만, 자주 사용하는 키워드를 우선 소개합니다.

- repository 또는 repo: 저장소 / Git으로 버전 관리하는 디렉토리를 의미
- local repository: 로컬 저장소 / 작업자의 개발 환경(PC)에 설정된 Git 저장소
- remote repository: 원격 저장소 / GitHub 등 외부 서버에 설정된 Git 저장소
- commit: 커밋 / 특정 상태를 기록한 것, 즉 버전을 의미
- branch: 브랜치 / 한국어로 번역하면 가지치기 또는 갈래라고 하는데 또 다른 작업공간을 의미
- merge: 머지 / 한국어로 병합 또는 합치기라고 하는데 특정 브랜치에서 작업한 내용을 또 다른 브랜치에 적용하는 것을 의미

---

## **git init - 저장소 만들기**

`it init`

- 로컬 Git 저장소를 설정합니다.

- 작업
- sample 디렉토리 생성
- red, orange 파일 추가
- sample 디렉토리를 로컬 저장소로 설정

- 실습

`mkdir sample`

`cd sample`

`touch red orange`

`echo "빨강" >> red`

`echo "주황" >> orange`

`git init`

- **mkdir, cd, touch, echo 명령어**

- 터미널 명령어를 소개합니다.

1. mkdir: 디렉토리 생성
2. cd: 디렉토리로 이동
3. touch: 빈 파일 생성
4. echo "[글자]" >> [파일]: 파일에 글자 추가

- 결과

`Initialized empty Git repository in /Users/cs.kim/Workspace/github.com/subicura/sample/.git/`

- sample 디렉토리에 Git 저장소 생성

  - 디렉토리 하위에 .git 디렉토리 생성 - Git과 관련된 정보 저장
  - 쉘 프롬프트가 ➜ sample에서 ➜ sample git:(main) ✗로 변경

  - main branch
  - 기본 브랜치 설정이 master인 경우 main 대신 master로 설정됩니다. 최근 master 대신 main을 쓰는 추세고 master로 설정되었다면 git branch -M main 명령어로 브랜치를 main으로 변경해주세요.

---

### **git status - 현재 상태 확인**

`git status`

- 현재 작업 중인 파일의 상태를 확인합니다.

  - 작업

1. **상태 확인**

실습

`git status # gst`

- gst 는 뭔가요?
- 명령어 뒤에 주석으로 써있는 부분은 alias로 oh-my-zsh을 설치하면 사용할 수 있는 별칭입니다.
- git status대신 gst만 입력해도 동일하게 동작합니다. alias를 적극적으로 써보세요!

  - 결과
    `On branch main`

  `No commits yet`

  `Untracked files:
(use "git add <file>..." to include in what will be committed)
orange
red`

  `nothing added to commit but untracked files present (use "git add" to track)`

- 현재 브랜치(main)와 커밋 상태, 작업 중인 파일의 상태 확인

  - untracked files(추적하지 않는 파일)이 존재하는 것을 확인

---

#### git add - 현재 상태 추적

`git add [-A] [<pathspec>…​]`

- 파일의 변경사항을 인덱스index에 추가합니다. Git은 커밋하기 전, 인덱스에 먼저 커밋할 파일을 추가합니다

  - 작업

  1. -A 옵션을 이용하여 전체 파일(orange, red)을 인덱스에 추가
  2. 상태 확인

  - 실습

  git add -A # gaa
  git status # gst

- 결과

`On branch main`

`No commits yet`

```Changes to be committed:
   (use "git rm --cached <file>..." to unstage)
     new file:   orange
     new file:   red
```

- untracked files에 있던 orange와 red의 상태가 변경된 것을 확인

---

##### **git commit - 현재 상태 저장**

`git commit [-m <msg>]`

- 인덱스에 추가된 변경 사항을 이력에 추가합니다.

- 작업

1. -m 옵션을 이용하여 첫 번째 이력에 대한 메시지 작성

- 실습
  `git commit -m "v1 commit" # gc -m "v1 commit"`

- 결과

`[main (root-commit) 25354ae] v1 commit
  2 files changed, 0 insertions(+), 0 deletions(-)
  create mode 100644 orange
  create mode 100644 red`

- 커밋을 생성했다!

- 새 파일 추가

- 앞에서 했던 것과 동일한 방식으로 yellow 파일을 추가합니다.

- 작업

  1. yellow 파일을 만듭니다.
  2. 상태 확인

- 실습
  touch yellow
  echo "노랑" >> yellow
  git status # gst

- 결과
  `On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
    yellow`

`nothing added to commit but untracked files present (use "git add" to track)`

- **새 파일 커밋**

- 작업

  1. 직전 커밋 이후 변경된 전체 파일(yellow)을 인덱스에 추가
  2. 두 번째 이력 커밋

- 실습
  `git add -A # gaa
git commit -m "v2 commit" # gc -m "v2 commit"`

- 현재 Git 저장소 이력
  첫번째 커밋(v1)---두번째 커밋(v2)

- **다양한 변화**

- 추가/수정/삭제를 이용한 세 번째 이력을 만듭니다.

- 작업

1. red 삭제
2. orange에 내용 추가
3. green 파일 추가
4. 상태 확인
5. 전체 파일 인덱스에 추가
6. 세 번째 이력 커밋

- 실습

```rm red
echo "오렌지" >> orange
touch green
git status # gst
git add -A # gaa
git commit -m "v3 commit" # gc -m "v3 commit"
```

- 결과

`On branch main
 Changes not staged for commit:
   (use "git add/rm <file>..." to update what will be committed)
   (use "git restore <file>..." to discard changes in working directory)
    modified:   orange
    deleted:    red`

`Untracked files:
  (use "git add <file>..." to include in what will be committed)
    green`

`no changes added to commit (use "git add" and/or "git commit -a")`

- orange를 수정했고 red는 삭제, green은 새로 만들어진 것을 확인
- 현재 Git 저장소 이력
  첫번째 커밋(v1)---두번째 커밋(v2)---세번째 커밋(v3)

---

#### **git log - 이력 확인**

`git log [<options>] [<revision range>] [[--] <path>…​]`

- git log는 다양한 옵션을 조합하여 원하는 형태의 로그를 출력할 수 있는 강력한 기능입니다. 이번 실습에선, 추가 옵션 없이 git log만 사용합니다.

- 작업

1. 전체 로그 확인

- 실습

  `git log`

- 결과

`commit 306b9474de0af37367ff90e5c1367588413f81bf (HEAD -> main)
 Author: subicura <subicura@subicura.com>
 Date:   Sat Jul 17 00:55:36 2021 +0900`

`v3 commit`

`commit 27a00b73cf7ab2e70e8dd5e5235bf7f94e9ddd84
 Author: subicura <subicura@subicura.com>
 Date:   Sat Jul 17 00:53:50 2021 +0900`

`v2 commit`

`commit 1ac5146ad27c5277996d54c08ec4ccded0edd4e3
 Author: subicura <subicura@subicura.com>
 Date:   Sat Jul 17 00:50:30 2021 +0900`

`v1 commit`

- 전체 커밋 로그 확인

---

##### **git push - 원격 저장소 저장**

`git remote add <name> <url>`

`git push [-u | --set-upstream] [<repository> [<refspec>…​]]`

- 앞에서 실습했던 로컬 저장소를 GitHub에 푸시합니다. 로컬 저장소의 커밋 목록이 그대로 복제될 예정입니다.

- 작업

1. main 브랜치에 원격 저장소(GitHub)를 origin(기본)으로 설정합니다.
2. 메인 브랜치를 main으로 설정합니다. (이미 main이므로 생략 가능)
3. 설정한 원격 저장소에 로컬 저장소의 모든 커밋을 푸시합니다. -u 옵션을 이용하여 이후에 푸시할 땐 별다른 원격 저장소 이름을 지정하지 않고 git push를 사용할 수 있습니다.

- **origin**

- Git은 여러 개의 원격 저장소를 등록할 수 있고 기본 저장소의 이름이 origin입니다. GitHub을 메인 원격 저장소(origin)로 사용하고 Google Cloud에 추가로 원격 저장소 설정을 한다면 google이라는 이름을 사용할 수 있습니다.

- 실습

- git remote add origin `https://github.com/subicura-git/sample.git`
- git branch -M main
- git push -u origin main # gp -u origin main

- 결과

`Username for 'https://github.com':
 Password for 'https://subicura-git@github.com':
 Enumerating objects: 24, done.
 Counting objects: 100% (24/24), done.
 Delta compression using up to 8 threads
 Compressing objects: 100% (15/15), done.
 Writing objects: 100% (24/24), 1.82 KiB | 1.82 MiB/s, done.
 Total 24 (delta 5), reused 0 (delta 0), pack-reused 0
 remote: Resolving deltas: 100% (5/5), done.
 To https://github.com/subicura-git/sample.git`
`* [new branch]      main -> main
 Branch 'main' set up to track remote branch 'main' from 'origin'.
 GitHub 저장소의 접근권한이 제한되어 있어 아이디, 패스워드를 입력하라고 합니다. 아이디, 패스워드를 입력하면  정상적으로 푸시가 완료됩니다.`

- GitHub 저장소의 접근권한이 제한되어 있어 아이디, 패스워드를 입력하라고 합니다. 아이디, 패스워드를 입력하면 정상적으로 푸시가 완료됩니다.

-**https vs ssh**

- 원격 저장소의 주소를 설정할 때, https와 ssh를 선택할 수 있습니다. https는 아이디/패스워드 방식을 사용하고 ssh는 개인키와 공개키를 이용합니다. 이번 실습에선 https 방식을 이용합니다.

- 푸시 후 GitHub 페이지를 새로고침 합니다.

![http](https://subicura.com/git/assets/img/github-push.ce6d3007.png)

- 로컬 저장소에서 작업한 내용이 똑같이 보이는 것을 확인할 수 있습니다. 여러 가지 메뉴를 눌러보면 CLI로 확인했던 사항을 웹으로 볼 수 있습니다.

- 이제 로컬 디렉토리를 지워도 원격에 동일한 저장소가 있기 때문에 언제든지 복구할 수 있습니다.

- **새 커밋 Push**

- 원격 저장소 연결 후, 로컬에서 navy 파일을 만들고 Push해 보겠습니다.

- 작업

1. navy 파일 추가
2. 전체 파일 인덱스에 추가
3. 새 커밋 작성
4. 원격 저장소에 푸시

- 실습

`touch navy
 echo "네이비" >> navy
 git add -A # gaa
 git commit -m "add navy" # gc -m "add navy"
 git push # gp`

- 확인

`Enumerating objects: 4, done.
 Counting objects: 100% (4/4), done.
 Delta compression using up to 8 threads
 Compressing objects: 100% (2/2), done.
 Writing objects: 100% (3/3), 264 bytes | 264.00 KiB/s, done.
 Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
 remote: Resolving deltas: 100% (1/1), completed with 1 local object.
 To https://github.com/subicura-git/sample.git
    a580ff2..33d9d23  main -> main`

- 이전에 했던 작업과 차이점은 마지막에 푸시를 한 것밖에 없습니다. Git은 로컬에서 대부분의 작업이 이루어지고 원격 저장소와 연동이 필요하다고 생각할 때 추가적인 작업을 하면 됩니다.

- 푸시 후 GitHub 페이지를 새로고침 합니다.

![gii](https://subicura.com/git/assets/img/github-push-2-1.78263006.png)

- 로컬 저장소에서 작업한 새로운 커밋과 파일이 추가된 것을 확인할 수 있습니다.

![wwi](https://subicura.com/git/assets/img/github-push-2-2.33ce7abb.png)

- 이력도 정상적으로 확인됩니다.

![gfds](https://subicura.com/git/assets/img/github-push-2-3.f34d948b.png)

- 커밋 변경사항도 확인할 수 있습니다.

---

##### **추가 커밋 Push**

- 현재 동일한 원격 저장소를 바라보는 두 개의 로컬 저장소가 있습니다. 하나의 저장소에서 변화를 주고 다른 저장소에서 변화를 동기화하는 작업을 해보겠습니다.

- 작업

1. sample 디렉토리로 이동 (여기서 작업하고 sample-2에서 확인할 예정)
2. purple 파일 추가
3. 전체 파일 인덱스에 추가
4. 새 커밋 작성
5. 원격 저장소에 푸시

- 실습

```git
cd sample
 touch purple
 echo "보라" >> purple
 git add -A # gaa
 git commit -m "add purple" # gc -m "add purple"
 git push # gp
```

- 확인

`[main cdce49d] add purple
  1 file changed, 1 insertion(+)
  create mode 100644 purple
 Enumerating objects: 4, done.
 Counting objects: 100% (4/4), done.
 Delta compression using up to 8 threads
 Compressing objects: 100% (2/2), done.
 Writing objects: 100% (3/3), 262 bytes | 262.00 KiB/s, done.
 Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
 remote: Resolving deltas: 100% (1/1), completed with 1 local object.`
`To https://github.com/subicura-git/sample.git'
33d9d23..cdce49d main -> main

- sample 로컬 저장소와 GitHub 저장소는 purple이 추가되어 있고, sample-2 저장소는 아직 추가되지 않은 상태입니다.

---

##### **git pull - 원격 저장소 내용 가져오기**

`git pull [<repository> [<refspec>…​]]`

- 원격 저장소에 변경된 내용을 로컬 저장소로 가져옵니다. Git은 자동으로 원격 저장소와 로컬 저장소를 동기화하지 않습니다. 명시적으로 명령어를 입력해야 합니다.

- 작업

1. sample-2 디렉토리로 이동
2. 원격 저장소 풀 명령어 입력

- 실습

`cd ..
 cd sample-2
 git pull # gl`

- 확인

`Updating 33d9d23..cdce49d
 Fast-forward
  purple | 1 +
  1 file changed, 1 insertion(+)
  create mode 100644 purple`

- sample-2 로컬 저장소에 purple 파일이 생긴 것을 확인할 수 있습니다.

- **Git Pull을 자주 하자**

- 원격 저장소와 로컬 저장소의 차이가 커지면 나중에 충돌이 많이 발생하기 때문에 Git Pull은 자주 수행하는 것이 좋습니다.
