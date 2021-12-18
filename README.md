# 📝 markdown-api-docs

## 📚 API 설계

###### API Reference

<details markdown="1">
<summary>자원</summary>

<details markdown="1">
<summary>/resources</summary>

**자원 등록**
----
새로운 자원을 등록합니다.

* **URL**

  /resources

* **Method:**

  `POST`

* **Data Params**

  **Required:**
 
  `name=[String] - 자원명`  
  `count=[Integer] - 수량`  

  **Optional:**

  `description=[String] - 자원 설명`  

* **Response**

  **Required:**

  `id=[String] - 자원 일련번호`  
  `name=[String] - 자원명`  
  `description=[String] - 자원 설명`  
  `count=[Integer] - 수량`    
  `created_at=[Date] - 생성 일자`

* **Success Response:**
```
HTTP/1.1 201 Created
Content-type: application/json;charset=UTF-8
{
  "id": "1",
  "name": "휴대폰",
  "description": "아이폰12",
  "count": 1,
  "created_at": "2018-07-04 14:00:00"
}
```

</details>

<details markdown="1">
<summary>/resources/{id}</summary>

**자원 상세 조회**
----
자원을 상세 조회합니다.

* **URL**

  /resources/:id

* **Method:**

  `GET`

* **Response**

  **Required:**  
  `id=[String] - 자원 일련번호`  
  `name=[String] - 자원명`  
  `description=[String] - 자원 설명`  
  `count=[Integer] - 수량`  

  **Optional:**   

* **Success Response:**
```
HTTP/1.1 200 OK
Content-type: application/json;charset=UTF-8
{
  "id": "1",
  "name": "휴대폰",
  "description": "아이폰",
  "count": 1,
}
```

**자원 삭제**
---- 
특정 자원을 삭제합니다.

* **URL**

  /resources/:id

* **Method:**

  `DELETE`

* **Success Response:**
```
HTTP/1.1 204 No Content
```

</details>
</details>

<details markdown="1">
<summary>에러 코드</summary>

**HTTP 상태 코드**
----

* **Response**

  `code=[Integer] - 에러 코드`  
  `message=[String] - 에러 메시지`

* **Success Response:**
```
HTTP/1.1 401 Unauthorized
{
  "errors": [
    {
      "status": "401",
      "message":  "Unauthorized"
    }
  ]
}
```

</details>
