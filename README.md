# π markdown-api-docs

## π API μ€κ³

###### API Reference

<details markdown="1">
<summary>μμ</summary>

<details markdown="1" style="margin-left:14px">
<summary>/resources</summary>

**μμ λ±λ‘**
----
μλ‘μ΄ μμμ λ±λ‘ν©λλ€.

* **URL**

  /resources

* **Method:**

  `POST`

* **Data Params**

  **Required:**
 
  `name=[String] - μμλͺ`  
  `count=[Integer] - μλ`  

  **Optional:**

  `description=[String] - μμ μ€λͺ`  

* **Response**

  **Required:**

  `id=[String] - μμ μΌλ ¨λ²νΈ`  
  `name=[String] - μμλͺ`  
  `description=[String] - μμ μ€λͺ`  
  `count=[Integer] - μλ`    
  `created_at=[Date] - μμ± μΌμ`

* **Success Response:**
```
HTTP/1.1 201 Created
Content-type: application/json;charset=UTF-8
{
  "id": "1",
  "name": "ν΄λν°",
  "description": "μμ΄ν°12",
  "count": 1,
  "created_at": "2018-07-04 14:00:00"
}
```

</details>

<details markdown="1" style="margin-left:14px">
<summary>/resources/{id}</summary>

**μμ μμΈ μ‘°ν**
----
μμμ μμΈ μ‘°νν©λλ€.

* **URL**

  /resources/:id

* **Method:**

  `GET`

* **Response**

  **Required:**  
  `id=[String] - μμ μΌλ ¨λ²νΈ`  
  `name=[String] - μμλͺ`  
  `description=[String] - μμ μ€λͺ`  
  `count=[Integer] - μλ`  

  **Optional:**   

* **Success Response:**
```
HTTP/1.1 200 OK
Content-type: application/json;charset=UTF-8
{
  "id": "1",
  "name": "ν΄λν°",
  "description": "μμ΄ν°",
  "count": 1,
}
```

**μμ μ­μ **
---- 
νΉμ  μμμ μ­μ ν©λλ€.

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
<summary>μλ¬ μ½λ</summary>

**HTTP μν μ½λ**
----

* **Response**

  `code=[Integer] - μλ¬ μ½λ`  
  `message=[String] - μλ¬ λ©μμ§`

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
