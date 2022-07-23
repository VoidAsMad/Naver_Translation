# Reference
* [Naver](https://github.com/VoidAsMad/Naver_Translation/blob/main/reference.md#naver)
* [Model](https://github.com/VoidAsMad/Naver_Translation/blob/main/reference.md#model)
* [Exception](https://github.com/VoidAsMad/Naver_Translation/blob/main/reference.md#exception)

## Naver
```py
class Translation(client_id : str, client_secret : str):
```
* 해당 라이브러리를 사용하려면 [네이버 개발자센터](https://developers.naver.com/main/)에서 발급받은 `Client ID`와 `Client Secret`가 필요합니다.
#### - Parameters
> **Client_ID** : 개발자센터에서 발급받은 `Client ID`를 입력합니다.<br/>
> **Client_Secret** : 개발자센터에서 발급받은 `Client Secret`를 입력합니다.

#### - func
```py
detect(text : str) -> NaverImage:
```
> 언어인식을 진행합니다. 입력한 글이 무슨 언어인지 인식하여 반환합니다.
```py
translation(text : str, target : str, source : str = None) -> NaverTranslation:
```
> 번역을 진행합니다.
> - Parameters<br/>
> **target** : 도착언어를 설정합니다. ([언어코드표](https://developers.naver.com/docs/papago/papago-nmt-api-reference.md#%ED%8C%8C%EB%9D%BC%EB%AF%B8%ED%84%B0))<br/>
> **source** : 출발언어를 입력합니다. ex) `ko`, `en` 비워둘시 자동으로 언어를 인식합니다.

## Model
```py
class NaverDetect:
```
언어인식을 실행했을시 반환되는 클래스입니다.<br/>
`text()` : str형태로 반환합니다.
`json()` : 원문형태로 반환합니다<br/>

```py
class NaverTranslation:
```
번역을 실행했을시 반환되는 클래스입니다.<br/>
`text()` : str형태로 반환합니다.<br/>
`json()` : 원문형태로 반환합니다<br/>
`src_lang_type()` : 출발언어를 반환합니다.<br/>
`tar_lang_type()` : 도착언어를 반환합니다.<br/>

## Exception
```py
class DetectError(Exception):
```
언어인식 API 응답코드가 200이 아닐때 생기는 오류입니다.
```py
class TranslationError(Exception):
```
번역 API 응답코드가 200이 아닐때 생기는 오류입니다.
