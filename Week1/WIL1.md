## WIL 1

### Git
- Git은 버전 관리 및 협업의 위해 사용하는 오픈소스 소프트웨어이다.
- Git에서는 어떤 파일이, 누가, 언제, 어떻게 수정됐는지를 추적하고 원하는 상태의 코드를 사용할 수 있습니다.

### 파일의 생명 주기
- 파일은 Untracked 상태와 Tracked 상태로 나뉘고 Tracked는 Unmodified, Modified, Staged 상태로 나뉩니다.

### GitHub
- GitHub는 코드 공유, 이슈 트래킹, 코드 리뷰, CI/CD 등을 위한 플랫폼이다.

### Git으로 파일 관리하기
- .git 폴더 만들어 디렉토리를 Git 저장소로 만들기
```
$ git init
```
- Git으로 관리할 대상 등록하기
    1. 모든 파일 한번에 등록
    ```
    $ git add .
    ```
    2. 하나씩 등록
    ```
    $ git add '<파일명>'
    ```
    3. unstage로 되돌리기
    ```
    $ git rm --cached '<파일명>'
    ```
- Git으로 파일 관리하기
    1. 파일 수정 후 로컬 저장소로 옮기기
    ```
    $ git commit -m "<commit message>"
    ```
    2. Commit Message - type
        * feat: 새로운 기능을 추가한 경우
        * refactor: 기존 코드를 개선한 경우
        * fix: 버그를 수정한 경우
        * chore: 코드 외의 설정을 바꾼 경우
        * docs: 문서화
        * test: 테스트 코드
- GitHub에 올리기
```
$ git push origin main
```

## Git/GitHub를 활용한 실습

<https://github.com/BOLRUP/BOLRUP>
