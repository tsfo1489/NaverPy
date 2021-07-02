# NaverPy
## Naver Open API Package

Naver의 Open API를 응용한 패키지 입니다

<hr>

## Example Code

### Constructor

```python
from NaverPy import API, Auth
auth = Auth(Client_ID. Client_Secret)
api = API(auth)
```

### Search API

```python
api.search('blog', 'Test', 'json', {'sort' : 'date'})
```

#### API.search(target, query, ext, arg)

##### target

검색 API의 종류 선택 Argument

> 'blog' : https://developers.naver.com/docs/serviceapi/search/blog
> 'news' : https://developers.naver.com/docs/serviceapi/search/news
> 'book' : https://developers.naver.com/docs/serviceapi/search/book
> 'encyc' : https://developers.naver.com/docs/serviceapi/search/encyc
> 'movie' : https://developers.naver.com/docs/serviceapi/search/movie
> 'cafearticle' : https://developers.naver.com/docs/serviceapi/search/cafearticle
> 'kin' : https://developers.naver.com/docs/serviceapi/search/kin

##### query

각 검색 API의 필수 변수

##### ext 

API의 파일 형식 선택(삭제예정)

##### arg

각 검색 API별 추가 옵션 설정