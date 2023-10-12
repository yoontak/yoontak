# Open Source_Lecture 6 (Hwang Yoontak_202334564)

## Changes Vs. Snapshots
**Changes** : 첫 번째 버전의 파일을 제외하고 버전이 지나서 생긴 변화사항은 각각의 버전에 변화된 점만 기록한다.  
**Snapshots** :  각 버전마다 변화가 생기면 실질적으로 생긴 변화를 전부 저장하여 각 버전에 저장한다.  

## Version Control
**Centralized Control** : 중앙 서버에 버전 정보를 저장한 후, 로컬 컴퓨터에서 필요 시 중앙 서버에 요청하면 중앙 서버에 기록된 버전 중 하나를 받아온다. 하지만 중앙 서버에만 버전에 대한 정보가 있기 때문에 중앙 서버가 다운되면 문제가 많아진다.  
**Distributed Control** : 중앙 서버에 버전 정보를 저장한 후, 각각의 로컬 컴퓨터에 버전 정보의 사본을 저장해둔다. 따라서 **Centralized Control**과 비교하여 중앙 서버가 다운되어도 버전에 대한 정보를 복구 할 수 있다.  

## Git configurations levels
**System level** : 시스템에 있는 모든 사용자와 레퍼지토리에 영향을 준다.  
**Gloval level** : 최근 사용자의 레퍼지토리에만 영향을 준다.  
**Local level** : 최근 레퍼지토리에만 영향을 준다.  

**각각의 레벨은 이전의 레벨을 덮어쓰기 때문에 local level, global level, system level 순서대로 적용된다.**  


## Config Commands
#### $ git init
> Git 저장소를 초기화한다. 이 명령어를 입력하면 파일에 .git/이라는 디렉토리가 생성된다.
#### $ git status
> Git 저장소 내의 현재 상태를 확인한다.
> 브랜치의 정보 제공
> 수정된 파일의 목록
> 커밋되지 않은 파일  
 **(git의 관심 밖이기 때문에 제거하거나 편집해도 문제가 되지 않는다.)**
#### $ git add [file_name]
> 특정 파일을 Git 저장소의 Staging area로 올리고 싶을 때 사용한다.
#### $ nano [file_name]
> 특정 파일(텍스트)의 편집기이다.
#### $ git add .
> 디렉토리에 있는 모든 파일을 커밋한다.
#### $ git rm -- cached [file_name]
> 입력한 파일을 다시 **unstaging** 한다.
#### $ git nano .gitignore
> 명령어가 아니다
> 처음엔 내용이 없는 빈 파일이지만, 텍스트 안에 파일 이름을 입력하면 그 파일은 영구히 제외된다.
#### git commit -m "commit message"
> 모든 작업을 마무리하고 수정한 상태로 새로운 **snapshot**으로 저장한다.
> **"commit message"** 에는 주석처럼 무엇에 관한 내용인지 적는 것이 좋다.
