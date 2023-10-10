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
