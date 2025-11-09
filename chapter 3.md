# 깃과 브랜치


## 03-1 브랜치란
같은 제품을 여러회사의 요구에 따라 다르게 개발해야 하는 상황이 발생했을 때(**문제상황**), 
깃의 브랜치는 코드를 여러 방향으로 나눠 개발(branch)했다가 나중에 필요할 때 합칠 수(merge) 있다(**해결책**).


## 03-2 브랜치 만들기 및 이동하기

### 브랜치 만들기 및 확인

'git branch name' //브랜치 제작
'git branch' //브랜치 확인
브랜치 파일 앞에 *가 붙어있으면 현재 작업하는 위치를 나타낸다.
브랜치를 추가하고 **git log**를 실행하면 (HEAD->main)이라고 표시된 곳에  (HEAD->main,apple(브랜치명))으로 나타난다. 저장소에 main과 apple브랜치가 있고 현재 작업 브랜치는 main이다.
'git long --oneline' //한 줄에 한 커밋씩 출력


### 브랜치 이동하기
'git switch name' //브랜치 이동

## 03-3 브랜치 정보 확인하기

### 브랜치 정보 확인 기능
git add . //현재 저장소에서 수정 내용이 있는 파일을 스테이지로 옮김
git log --branches //브랜치들의 최신 커밋을 출력
git long --oneline --branches --graph //브랜치와 커밋 관계를 그래프로 제시 (**점선으로 부모와 자식 관계를 알 수 있음**)


### 브랜치 간 차이 확인 기능
'git long name1..name2' //왼쪽에 있는 브랜치를 기준으로 오른쪽 브랜치와 비교 (**오른쪽에 있는 것만 제시**)


## 03-4 브랜치 병합하기

1. 'git merge name' //name브랜치를 현재 브랜치에 병합
위 명령어를 실행하면 'Merge branch name'이라는 커밋 메시지가 나타난다.
2. ls -al
   명령어를 실행하면 name 브랜치에 있던 파일이 현재 브랜치에 합쳐진다.


### 같은 문서에서 서로 다른 문서를 수정했을 때

-'Merge branch name'이라는 커밋 메시지가 나타난다.
-cat을 통해 파일을 출력하면 name과 현재 브랜치의 수정 내용이 하나의 파일에 합쳐진다.


### 서로 다른 브랜치에서 한 문서의 같은 부분을 수정했을 때

-빔이 열리지 않고 경고 메시지가 나타난다.
'CONFLICT (content): Merge conflict in A.txt'
'Automatic merge failed; fix conflicts and then commit the result.'
-vim을 통해 A.txt파일을 열어보면

<<<<<<< HEAD
present file content B
=======
name content C
>>>>>>> name
>>>>>>>

위와 같은 코드가 발생한다.


### 브래치 삭제

'git branch -d name' //병합한 브랜치 삭제
'git branch -D name' //병합하지 않은 브랜치 삭제


### cherry-pick으로 병합하기

특정 버전의 변경 내용만 합치려고 할 때 사용
'git cherry-pick <해시>' //해시에 있는 파일의 변경 내용이 현재 파일에 추가


##문제 풀이

1. git branch fixed
2. git switch fixed
3. git log --oneline
4. git add .
5. git log --branches --graph
6. cat edit.txt
7. git init doit
8. git merge fixed
9. git branch -d fixed
