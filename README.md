# Restful_practice

Restful api 개념 정리 및 실습

## Representational State Transfer

인터넷 상의 통신에서 쓰이는 아키텍쳐 스타일이다. RWS(RESTful Web Service)를 따르는 웹 서비스는 통신간 HTML, XML, JSON 형태의 파일을 주고 받으며 정해진 규약을 따르며 코드를 작성한다. 클라이언트에서 GET, POST, PUT, DELETE 등 다양한 메소드를 통해 http 요청을 작성하고 서버의 응답을 받는다.

## CRUD Operations

create, read, update, delete의 데이터를 사용함에 있어 필수적인 요소들을 이야기하는 것이다. HTTP 통신간 각 요소들은 method로 header에 작성하여 요청한다.

## HTTP METHODS

- GET: getting data
- Post: creating data
- PUT: Updating data
- DELETE: deleting data

### Multiple data requests

Request

```
Get /api/customers
```

Response

```
[
  { id: 1, name: '' },
  { id: 2, name: '' },
  ...
]
```

### Single data requests

#### GET a customer

Request

```
Get /api/customers/**1**
```

Response

```
{ id: 1, name: '' }
```

=> id를 통해서 해당 정보를 얻을 수 있다.

#### PUT a customer

Request

```
PUT /api/customers/1

{name: 'B-SENS'}
```

Response

```
{ id: 1, name: 'B-SENS' }
```

=> id를 통해서 해당 정보를 변경 할 수 있다.

#### DELETE a customer

Request

```
DELETE /api/customers/1
```

Response

```

```

=> id를 통해서 해당 정보를 삭제 할 수 있다.

#### CREATE a customer

Request

```
POST /api/customers
{ name: 'B-SENS' }
```

Response

```
{id: 1, name: 'B-SENS'}
```

=> id를 통해서 해당 정보를 삭제 할 수 있다.
