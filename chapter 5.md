# 깃허브로 협업하기

## 05-1 서로 다른 컴퓨터에서 원격 저장소 함께 사용하기  
``` bash
git clone 원격 저장소 주소 지역 저장소//원격 저장소를 지역 저장소에 복사
```
git_home에서 (commit -> push) 과정을 이행하면 원격 저장소에 정보가 입력됨  
git_office에서 (pull)을 이행하면 원격 저장소에 입력된 정보가 git_office에 저장됨  
  
**pull과 push를 습관화하여 항상 최신 소스 유지 필요**

## 05-2 원격 브랜치 정보 가져오기  
``` bash
git fetch // 원격 저장소에서 최신정보를 가져오기만 함
git merge // 브랜치 2개를 합침
git pull // 최신 커밋을 가져오고(fetch) + 현재 브랜치에 합침(merge)
```

## 05-3 협업의 기본 알아보기  
### -브랜치 생성
여러 사람이 소스 코드를 올리면 서로 꼬일 수 있기 때문에 이를 방지하기 위하여,  
사용자별로 브랜치를 만들어 각자 자신의 브랜치를 만들어 커밋을 올리고 다른 사람의 허가를 받아 main브랜치에 합친다.  
### -공동 작업자 추가  
공동 작업자의 이메일 주소를 입력하여 커밋을 올릴 수 있는 권한을 가지게 된다.  

## 05-4 원격 저장소에서 협업하기  
### 원격 저장소 저장
``` bash
git clone github.com/A/B.git //A라는 사람이 만든 이름이 B인 저장소를 현재 위치한 폴더 아래에 저장
```
### 풀 리퀘스트 보내기 및 병합
풀 리퀘스트(pull request): 내가 만든 코드를 상대방에게 pull해달라고 request하는 것 (커밋의 메시지를 남기는 것)  
**과정**
커밋 -> 브랜치에 푸시 -> Contribute -> Open pull request  
-> 메시지 작성 -> Create pull request => 저장소에 풀 리퀘스트 전송  

  ### <참고>  
<img width="163" height="135" alt="image" src="https://github.com/user-attachments/assets/8d655e8b-4d53-4023-9644-3918b5cd753c" />**가 붙은 것은 Open 풀 리퀘스트 // 아직 마무리 되지 않은 풀 리퀘스트**  

  풀 리퀘스트 메시지를 보고 문제 없으면 Merge pull request 클릭해 병합 -> 성공적으로 병합됬다는 메시지가 나오면 병합 성공!  

    
### <참고>  
<img width="291" height="70" alt="image" src="https://github.com/user-attachments/assets/094bab72-d1e3-4d70-9d3a-6bed2674f370" /> **병합에 성공하면 Merged로 바뀜**
  
## 문제풀이
git clone 원격 저장소.git myhome  
git fetch  
git pull  
git diff  
git config user.name  
git config user.email  
git push -u origin apple  
풀 리퀘스트
