### 231010
## userdel 로 인해 home dir 가 날라갔을 때...
### useradd 해서 다시 만들어줘야 한다.
```
useradd -r -u 2100 -g jhshin jhshin
```
### <br/>

### 그 다음 home dir 생성해주고 chown 으로 소유자 변경
```
mkdir /home/jhshin
chown jhshin: -R /home/jhshin
```
### <br/>

### usermod 로 home dir 설정
사용법
|||
|---|---|
|usermod <계정> -l <바꿀 계정>|계정명을 바꿀 계정명 으로 변경합니다. (사용 비 권장)|
|usermod -c <"이름"> <계정>|계정의 이름을 변경합니다.|
|usermod -d <"경로"> <계정>|계정의 홈 디렉터리를 변경합니다.|
|usermod -s <"셸"> <계정>|계정의 로그인 기본 셸을 변경합니다.|
usermod -e <날짜> <계정>
계정이 해당 날짜에 만료되도록 합니다.
ex) usermod -e 2018-05-01 myuser
usermod -g <그룹> <계정>	
사용자의 기본 소속 그룹을 변경합니다.
usermod -G <그룹> <계정>
계정의 소속 그룹을 변경합니다.
만약 여러 그룹을 지정할 때에는 ,(콤마) 로 구분하여 지정합니다.
usermod -a -G <그룹> <계정>	
계정의 소속 그룹을 추가(add) 합니다.
