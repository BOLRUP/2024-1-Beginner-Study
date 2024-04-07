## <p style="text-align:center;">개발 입문 스터디 Quiz 1</p>

#### Example
GDSC는 무엇의 약자인지 적으시오.

- 답: Google Developer Student Clubs

### Q1
Git에서 파일의 상태는 크게 untracked와 tracked로 나눌 수 있다.  
그렇다면 tracked에는 어떤 상태가 있는지 모두 적으시오.

- 답: Unmodified, Modified, Staged

### Q2
Git에는 세 가지 영역이 있다.  
세 가지 영역을 모두 나열하시오.

- 답: Working Directory, Staging Area, Local Repo

### Q3
현재 우리는 ```main```브랜치에 있다.  
```develop```이라는 브랜치를 새로 만들고 이동까지 한번에 할 수 있는 명령어를 적으시오.

- 답: git checkout -b "develop"

### Q4
Working Directory에 있는 파일들을 모두 Staging Area에 추가할 수 있는 명령어를 적으시오.

- 답: git add .

### Q5
```
1. Create a merge commit
2. Squash and merge
3. Rebase and merge
```
위의 세 가지가 어떤 차이가 있는지 간단히 적으시오.

- 답: ```1번```은 분리한 branch의 commit기록이 살아 있고 main branch와의 공통분모의 commit을 만들어 통합 ```2번```은 분리한 branch에서의 commit내용이 통합된 commit하나로 main branch와 통합 ```3번```은 분리한 branch의 commit 내용을 main branch에 새로 commit을 생성 그래서 commit hash가 변경됨

### Q6
```git log --oneline```으로 commit의 기록을 확인해보니  
첫 줄에 ```a1s2d3f (HEAD -> develop) docs: readme 추가```라는 log가 찍혔다.
알 수 있는 사실을 모두 적으시오.

- 답: 가장 최근의 commit, ```a1s2d3f```는 commit id, ```(HEAD -> develop)```로는 현재 ```develop```이라는 branch에서 작업 중이고 다음 commit의 base가 ```develop```이다. ```docs: readme 추가```는 commit message로 readme 문서파일을 추가했다는 내용이다.

### Q7
```git log --oneline```으로 commit의 기록을 확인해보니 아래와 같은 log를 확인 할 수 있었다.  
```
a1s2d3f (HEAD -> develop) fifth commit
s2d3f4g fourth commit
345hj26 third commit
7g8dg7f second commit
5g568vk first commit
```
이때, fourth commit까지 제거하고 fourth commit과 fifth commit의 변경 사항은
Staging Area에 남아 있길 바란다면 reset을 어떤 옵션과 함께 사용하면 되는지 적으시오.

- 답: git reset --soft 345hj26

### Q8
```git log --oneline```으로 commit의 기록을 확인해보니 아래와 같은 log를 확인 할 수 있었다.
```
a1s2d3f (HEAD -> develop) fifth commit
s2d3f4g fourth commit
345hj26 third commit
7g8dg7f second commit
5g568vk first commit
```
reset은 너무 위험하니 revert를 사용하려고 하여 ```fifth commit```을 되돌리고 싶다면 
어떤 명령어를 사용하면 되는지 적으시오. 

- 답: git revert a1s2d3f

### Q9
여러 사람이 협업하는 프로젝트에서 커밋을 되돌려야 한다.  
reset과 revert 중에 어떤 것을 선택할 것인지를 그 이유와 함께 적으시오.

- 답: revert, 왜냐하면 commit을 제거하지 않고 되돌리기 위한 새로운 commit이 작성되기 때문에 commit을 공유하는 다른 branch에 영향을 덜 주기 때문에
