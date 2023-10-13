### 231013
## 리눅스에서 이메일 보내는 방법
### 먼저 mutt 에 대한 기본 세팅이 되어 있어야 한다.
### smtp 프로토콜을 사용하고, 해당 프로토콜에 대한 정보를 적어주면 된다. 이 내용은 다른 블로그들을 참고하자
- https://comengx.tistory.com/30
- https://itsyouuu.tistory.com/112
### <br/>


### test.txt
```
test
```
### <br/>


### 이메일 보내는 방법
- -a : 파일을 첨부할 수 있다.
- -c : 참조
- -b : 숨은 참조
```
mutt -e "my_hdr From:no-reply@theragenbio.com" -s test jonghwan.shin@theragenbio.com < test.txt

# 파일 첨부 방법
mutt -e "my_hdr From:no-reply@theragenbio.com" -s test jonghwan.shin@theragenbio.com < test.txt -a [첨부 파일]
```
