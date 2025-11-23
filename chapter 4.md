# 깃허브 시작하기

## 04-1 원격저장소와 깃허브
깃에서는 지역 저장소와 원격 저장소를 연결해서 파일을 쉽게 백업할 수 있다  

  -원격 저장소로 할 수 있는 것  
  1. 원활한 협업 프로젝트에 용이
  2. 자신의 개발 이력을 남김
  3. 다른 사람의 소스를 살펴볼 수 있고, 오픈소스에 참여 가능

  ## 04-2 깃허브 가입하기  
  push: 지역 저장소에서 원격 저장소로 커밋하는 것  
  pull: 원격 저장소의 변경사항을 지역 저장소로 내려 받는 것  

  ## 04-3 지역 저장소를 원격 저장소에 연결하기  
  ``` bash
git remote add origin 'address' //지역 저장소를 원격 저장소에 연결
```
  ``` bash
git remote -v // 지역 저장소가 원격 저장소와 연결되어 있는지 보여줌, v==verbose
```
 ## 04-4 지역 저장소와 원격 저장소 동기화하기  
 ### -지역 저장소 -> 원격 저장소
  ``` bash
git push -u origin master // 지역 저장소를 원격 저장소에 처음 push할때 사용
git push // push명령어
```
### -원격 저장소-> 지역 저장소
  ``` bash
git pull origin master // 원격 저장소에서 커밋
```
## 04-5 깃허브에 SSH 원격 접속하기  
### -SSH 원격 접속 구축 과정
1. 프라이빗 퍼블릭 키 제작
  ``` bash
ssh-keygen // 퍼블릭 키와 프라이빗 키 제작 
```
-알아둘 점  
id_rsa // 프라이빗 키  
id_rsa.pub // 퍼블릭 키  

2. Github에 프라이빗 키 저장
3. 로그인 시 Github가 퍼즐 전송
4. 로컬 컴퓨터는 프라이빗 키로 퍼즐 해결
5. 해결하면 push/pull 사용 가능
### -SSH 원격 접속 이점
1.  비밀번호 입력 X
2.  개인키만 있으면 자동 로그인

## 문제풀이
git remote add origin 'address'  
git remote -v  
git push -u origin master  
git push  
git pull  
ssh-keygen
