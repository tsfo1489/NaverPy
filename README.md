# NaverPy
## Naver Open API Package

Naver의 Open API를 응용한 패키지 입니다

<hr>

## Example Code

Constructor

```python
from NaverPy import API, Auth
auth = Auth(Client_ID. Client Secret)
api = API(auth)
```

Search API

```python
api.search(target, query, ext, arg)
```