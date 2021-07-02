# NaverPy
## Naver Open API Package

Naver의 Open API를 응용한 패키지 입니다
현재 Datalab 트렌드 검색, 검색, 단축 URL 기능을 지원합니다

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
자세한 내용은 <a href='https://developers.naver.com/docs/serviceapi/search/blog/blog.md'>Naver Open API</a> 참조

> 'blog' : https://developers.naver.com/docs/serviceapi/search/blog/blog.md
> 'news' : https://developers.naver.com/docs/serviceapi/search/news/news.md
> 'book' : https://developers.naver.com/docs/serviceapi/search/book/book.md
> 'encyc' : https://developers.naver.com/docs/serviceapi/search/encyc/encyc.md
> 'movie' : https://developers.naver.com/docs/serviceapi/search/movie/movie.md
> 'cafearticle' : https://developers.naver.com/docs/serviceapi/search/cafearticle/cafearticle.md
> 'kin' : https://developers.naver.com/docs/serviceapi/search/kin/kin.md

##### query

각 검색 API의 필수 변수

##### ext 

API의 파일 형식 선택(삭제예정)

##### arg

각 검색 API별 추가 옵션 설정

### ShortUrl

```python
API.ShortUrl('http://d2.naver.com/helloworld/4874130')
```

#### ShortUrl(url)

API resonse를 json(python dict)형태로 return

```python
{
    "message":"ok",
    "result": {
        "hash":"GyvykVAu",
        "url":"https://me2.do/GyvykVAu",
        "orgUrl":"http://d2.naver.com/helloworld/4874130"
    }
    ,"code":"200"
}
```

