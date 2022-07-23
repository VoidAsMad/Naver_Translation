## 빠른시작

### 글자인식하기
```py
from naver_translation import naver

#로그인 진행
naver = naver.Translation(client_id = "Client_ID", client_secret = 'Client_Secret')
result = naver.detect(text = '너구리').text()

print(result)
```

### 번역
```py
from naver_translation import naver

#로그인 진행
naver = naver.Translation(client_id = "Client_ID", client_secret = 'Client_Secret')
result = naver.translation(text = 'hello', target = "ko").text()

print(result)
```
