# Quest 00. 형상관리 시스템

## Introduction
* git은 2021년 현재 개발 생태계에서 가장 각광받고 있는 버전 관리 시스템입니다. 이번 퀘스트를 통해 git의 기초적인 사용법을 알아볼 예정입니다.

## Topics
* git
  * `git clone`, `git add`, `git commit`, `git push`, `git pull`, `git branch`, `git stash` 명령
  * `.git` 폴더
* GitHub

## Resources
* [Resources to learn Git](https://try.github.io)
* [Learn Git Branching](https://learngitbranching.js.org/?locale=ko)
* [Inside Git: .Git directory](https://githowto.com/git_internals_git_directory)

## Checklist
1. 형상관리 시스템은 왜 나오게 되었을까요?
 </br>‣ 소프트웨어의 변경사항을 체계적으로 관리하기 위해서 등장하였다.
 </br>‣ 변경사항을 통제/추적 가능 
 </br>‣ 변경된 내용에 대한 원인/변경사항 확인 가능

2. git은 어떤 형상관리 시스템이고 어떤 특징을 가지고 있을까요? 분산형 형상관리 시스템이란 무엇일까요?
  </br>‣ git은 분산형 버전 관리 시스템의 한 종류이다. 빠른 수행 속도가특징이다. 분산형 형상관리 시스템이란 모든 PC가 저장소가 될 수 있다. 즉, 중앙서버에 접속하지 않은 상태에서도 코드작업을 할 수 있다는 뜻이다. 
   * git은 어떻게 개발되게 되었을까요? git이 분산형 시스템을 채택한 이유는 무엇일까요?
  </br>‣ git은 사유 소스 관리 시스템인 비트키퍼 자유 이용이 막히면서 개발되게 되었다. git은 빠른 속도, 단순한 구조, 비선형적인 개발, 완벽한 분산을 위하여 분산형 시스템을 채택하였다.
  
3. git과 GitHub은 어떻게 다를까요?
</br>‣ git은 소스 코드를 기록을 관리하고 추적할 수 있는 버전 제어 시스템이고 github는 git 저장소를 관리할 수 있는 클라우드 기반 호스팅 서비스이다.

5. git의 clone/add/commit/push/pull/branch/stash 명령은 무엇이며 어떨 때 이용하나요? 그리고 어떻게 사용하나요?
</br>‣ clone :
</br>‣ add :
</br>‣ push :
</br>‣ pull :
</br>‣ branch :
</br>‣ stash : 임시 저장

7. git의 Object, Commit, Head, Branch, Tag는 어떤 개념일까요? git 시스템은 프로젝트의 히스토리를 어떻게 저장할까요?
</br>‣ Object
</br>‣ Commit
</br>‣ Head
</br>‣ Branch
</br>‣ Tag는

9. 리모트 git 저장소에 원하지 않는 파일이 올라갔을 때 이를 되돌리려면 어떻게 해야 할까요?

## Quest
* GitHub에 가입한 뒤, [이 커리큘럼의 GitHub 저장소](https://github.com/KnowRe-Dev/WebDevCurriculum)의 우상단의 Fork 버튼을 눌러 자신의 저장소에 복사해 둡니다.
* Windows의 경우 같이 설치된 git shell을, MacOSX의 경우 터미널을 실행시켜 커맨드라인에 들어간 뒤, 명령어를 이용하여 복사한 저장소를 clone합니다.
  * 앞으로의 git 작업은 되도록 커맨드라인을 통해 하는 것을 권장합니다.
* 이 문서가 있는 폴더 바로 밑에 있는 sandbox 폴더에 파일을 추가한 후 커밋해 보기도 하고, 파일을 삭제해 보기도 하고, 수정해 보기도 하면서 각각의 단계에서 커밋했을 때 어떤 것들이 저장되는지를 확인합니다.
* `clone`/`add`/`commit`/`push`/`pull`/`branch`/`stash` 명령을 충분히 익혔다고 생각되면, 자신의 저장소에 이력을 push합니다.

## Advanced
* Mercurial은 어떤 형상관리 시스템일까요? 어떤 장점이 있을까요?
* 실리콘밸리의 테크 대기업들은 어떤 형상관리 시스템을 쓰고 있을까요?
