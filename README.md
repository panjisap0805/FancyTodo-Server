# FancyTodo-Server

  Deploy Here:

[FancyTodo_Server](http://localhost:3000)

## API Documentation

----
  **Create Todo**
----
  Add a new todo in FancyTodo app

* **URL**

  /todos

* **Method:**

  `POST`

* **Request Headers**

  | key | value | required |
  | :---: | :---: | :---: |
  | Content-Type | application/x-www-form-urlencoded | true |

* **URL Params**

   none

* **Data Params**

  | key | value | required |
  | :---: | :---: | :---: |
  | title | <YOUR_TITLE> | true |
  | description | <YOUR_DESCRIPTION> | true |
  | status | <YOUR_STATUS> | true |
  | due_date | <YOUR_DUE_DATE> | true |

* **Success Response:**


  * **Code:** 201 CREATED <br />
    **Content:**
    ```json
    {
      "title": "Belajar",
      "description": "Belajar ngoding",
      "status": "On Progess",
      "due_date": 2019-12-31 17:00:00.000 +00:00
    }
    ```

* **Error Response:**

    * **Code:** 400 BAD REQUEST <br />
        **Content:**
        ```json
        ["please fill the title field"]
        ```

        OR

        ```json
        ["please fill the description field"]
        ```

        OR

        ```json
        ["please fill the status field!"]
        ```

        OR

        ```json
        ["please fill the due date field"]
        ```
    
    OR

    * **Code:** 500 INTERNAL SERVER ERROR <br />
        **Content:** 
        ```json
        { "error" : "Internal server error" }
        ```

----
  **Read All Todo**
----
  View all todo list

* **URL**

  /todos

* **Method:**

  `GET`

* **Request Headers**

  | key | value | required |
  | :---: | :---: | :---: |
  | Content-Type | application/x-www-form-urlencoded | true |

* **URL Params**

   none

* **Data Params**

   none

* **Success Response:**


  * **Code:** 201 CREATED <br />
    **Content:**
    ```json
    [
      {
        "id": 1,
        "title": "Belajar",
        "description": "Belajar ngoding",
        "status": "On Progess",
        "due_date": 2019-12-31 17:00:00.000 +00:00
      },
      {
        "id": 2,
        "title": "Belajar",
        "description": "Belajar ngoding",
        "status": "On Progess",
        "due_date": 2019-12-31 17:00:00.000 +00:00
      }
    ]
    ```

* **Error Response:**

    * **Code:** 500 INTERNAL SERVER ERROR <br />
        **Content:** 
        ```json
        { "error" : "Internal server error" }
        ```

----
  **Read a Todo**
----
  Find a todo by ID

* **URL**

  /todos/:id

* **Method:**

  `GET`

* **Request Headers**

  | key | value | required |
  | :---: | :---: | :---: |
  | Content-Type | application/x-www-form-urlencoded | true |

* **URL Params**

   | key | value | required |
   | :---: | :---: | :---: |
   | id | <YOUR_ID> | true |

* **Data Params**

   none

* **Success Response:**


  * **Code:** 200 OK <br />
    **Content:**
    ```json
    [
      {
        "title": "Belajar",
        "description": "Belajar ngoding",
        "status": "On Progess",
        "due_date": 2020/7/9
      }
    ]
    ```

* **Error Response:**

    * **Code:** 404 NOT FOUND <br />
        **Content:** 
        ```json
        { "error" : "Not found" }
        ```

----
  **Update Todo**
----
  Update an existing todo in FancyTodo app

* **URL**

  /todos/:id

* **Method:**

  `PUT`

* **Request Headers**

  | key | value | required |
  | :---: | :---: | :---: |
  | Content-Type | application/x-www-form-urlencoded | true |

* **URL Params**

   | key | value | required |
   | :---: | :---: | :---: |
   | id | <YOUR_ID> | true |

* **Data Params**

  | key | value | required |
  | :---: | :---: | :---: |
  | title | <YOUR_TITLE> | true |
  | description | <YOUR_DESCRIPTION> | true |
  | status | <YOUR_STATUS> | true |
  | due_date | <YOUR_DUE_DATE> | true |

* **Success Response:**


  * **Code:** 200 OK <br />
    **Content:**
    ```json
    {
        "title": "Belajar",
        "description": "Belajar ngoding",
        "status": "On Progess",
        "due_date": 2019-12-31 17:00:00.000 +00:00
    }
    ```

* **Error Response:**

    * **Code:** 400 BAD REQUEST <br />
        **Content:**
        ```json
        ["please fill the title field"]
        ```

        OR

        ```json
        ["please fill the description field"]
        ```

        OR

        ```json
        ["please fill the status field!"]
        ```

        OR

        ```json
        ["please fill the due date field"]
        ```
    
    OR

    * **Code:** 500 INTERNAL SERVER ERROR <br />
        **Content:** 
        ```json
        { "error" : "Internal server error" }
        ```
    
    OR

    * **Code:** 404 NOT FOUND <br />
        **Content:** 
        ```json
        { "error" : "Data not found" }
        ```

    OR

    * **Code:** 500 INTERNAL SERVER ERROR <br />
        **Content:** 
        ```json
        { "error" : "Internal server error" }
        ```

----
  **Delete Todo**
----
  Delete an existing todo in FancyTodo app

* **URL**

  /todos/:id

* **Method:**

  `DELETE`

* **Request Headers**

  | key | value | required |
  | :---: | :---: | :---: |
  | Content-Type | application/x-www-form-urlencoded | true |

* **URL Params**

   | key | value | required |
   | :---: | :---: | :---: |
   | id | <YOUR_ID> | true |

* **Data Params**

  none

* **Success Response:**


  * **Code:** 200 OK <br />
    **Content:**
    ```json
    {
      "title": "Belajar",
        "description": "Belajar ngoding",
        "status": "On Progess",
        "due_date": 2019-12-31 17:00:00.000 +00:00
    }
    ```

* **Error Response:**

    * **Code:** 404 NOT FOUND <br />
        **Content:** 
        ```json
        { "error" : "Not found" }
        ```

    OR

    * **Code:** 500 INTERNAL SERVER ERROR <br />
        **Content:** 
        ```json
        { "error" : "Internal server error" }
        ```
----
  **User Register**
----
  Register a new User to use application feature

* **URL**

  /user/register

* **Method:**
  
  `POST`

* **Request Headers**

  none
  
* **URL Params**

  none

* **Data Params**

  | key | value | required |
  | :---: | :---: | :---: |
  | email | <YOUR_EMAIL> | true |
  | password | <YOUR_PASSWORD> | true |

* **Success Response:**
  
  
  * **Code:** 201 CREATED <br />
    **Content:** 
    ```json
    {
    "id": 1,
    "email": "test@mail.com",
    "password": "$2a$05$d3aV7sATu.GowtpxqG6HoOMp3pTI53JVsw/CHhIiZefwtYlOl9JMm"
    }
    ```
 
* **Error Response:**

    * **Code:** 400 BAD REQUEST <br />
        **Content:** 
        ```json
        {
          "code": "400",
          "message": [
              "Please fill the email field"
          ]
        }
        ```

        OR

        ```json
        {
          "code": "400",
          "message": [
              "Use email format"
          ]
        }
        ```

        ```json
        {
          "code": "400",
          "message": [
              "Email already in use"
          ]
        }
        ```

        OR

        ```json
        {
          "code": "400",
          "message": [
              "Please fill the password field"
          ]
        }
        ```

    OR

    * **Code:** 500 INTERNAL SERVER ERROR <br />
        **Content:** 
        ```json
        {
          "code": "500",
          "message": "Internal Server Error"
        }
        ```
----
  **User Login**
----
  Login to access application feature

* **URL**

  /user/login

* **Method:**
  
  `POST`

* **Request Headers**

  none
  
* **URL Params**

  none

* **Data Params**

  | key | value | required |
  | :---: | :---: | :---: |
  | email | <YOUR_EMAIL> | true |
  | password | <YOUR_PASSWORD> | true |

* **Success Response:**
  
  
  * **Code:** 200 OK <br />
    **Content:** 
    ```json
    {
    "token": ""
    }
    ```
 
* **Error Response:**

    * **Code:** 400 BAD REQUEST <br />
        **Content:** 
        ```json
        {
          "code": "400",
          "message": "invalid email/password"
        }
        ```
    OR

    * **Code:** 500 INTERNAL SERVER ERROR <br />
        **Content:** 
        ```json
        {
          "code": "500",
          "message": "Internal Server Error"
        }
        ```