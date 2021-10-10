## 20211010 장원용 프로
### Git
- stash, working directory, staging area, local repository, remote repository 의 영역이 있다
- git add 등 staging area에 넣어두면 git 이 트래킹 가능하다
- 커밋을 할 경우 local repository 에 들어가고 push 를 할 경우 remote repository 로 반영된다
- Merge 에는 3-way merge 혹은 fast forward 방식으로 merge 된다
- 커밋을 옮기는 방식 즉 위치만 옮기는 방식을 fast forward 로 보면 된다
- 마스터로부터 피처 브랜치가 여러개 생겼을 경우, fast forward 가 불가능하고 브랜치별로 머지하는 방식인 3-way merge 를 하게 된다
- squash ( --squash ) : Squash 는 여러 개의 커밋을 하나로 합치는 기능을 말하며 머지할 브랜치 커밋을 하나의 커밋으로 합친 뒤 타겟 브랜치에 커밋하는 방식으로 머지를 진행한다
- 자잘한 커밋 사항이 남지 않기 때문에 변경사항을 읽기가 수월해지지만, 아무래도 정보력이 떨어질 수 있다
- rebase interactive
  - Rebase 는 브랜치의 공통 조상이 되는 base 를 다른 브랜치의 커밋 지점으로 바꾸는 것이다
  - 마치 master 에서 일렬로 커밋이 난 것 처럼 옮기고 싶을 경우에 rebase 를 사용한다
  - rebase 는 공통조상을 바꾼다는 뜻이다
  - 단일 브랜치 내에서 rebase 를 사용하여 커밋 히스토리를 합칠 수 있다, 이를 rebase interactive 라 한다
  - HEAD~3 과 같은 명령어를 통해 특정 커밋들을 rebase 시킬 수 있으며 이 과저에서 pick 과 같은 명령어를 통해 커밋을 재정렬하는 등 조정이 가능하다

- https://wonyong-jang.github.io/git/2021/02/05/Github-Merge.html
