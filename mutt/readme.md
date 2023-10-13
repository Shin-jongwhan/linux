### 231013
## 리눅스에서 이메일 보내는 방법
### 먼저 mutt 에 대한 기본 세팅이 되어 있어야 한다.
### test.txt
```
test
```
### <br/>

### 이메일 보내는 방법
### -a 옵션을 주면 파일을 첨부할 수 있다.
```
mutt -e "my_hdr From:no-reply@theragenbio.com" -s test jonghwan.shin@theragenbio.com < test.txt

# 파일 첨부 방법
mutt -e "my_hdr From:no-reply@theragenbio.com" -s test jonghwan.shin@theragenbio.com < test.txt -a [첨부 파일]
```
