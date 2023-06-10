### Register
- Method

  POST

- URL

  /register

- Body Request
  ```json
  {
    "name": "test",
    "email": "test@email.com",
    "pass": "password"
  }
  ```
- Response
  ```json
  {
    "status": "success",
    "message": "User created successfully"
  }
  ```

### Login
- Method

  POST

- URL

  /login

- Body Request
  ```json
  {
    "email": "test@email.com",
    "pass": "password"
  }
  ```
- Response
  ```json
  {
    "status": "success",
    "message": "login successful",
    "data": {
        "token": "<token>"
    }
  }
  ```

### Read User
- Method

  GET

- URL

  /readUser

- Headers

  Key = Authorization
  Value = Bearer <token from login>

- Response
  ```json
  {
    "status": "success",
    "message": "read successful",
    "data": {
        "user_id": <user id>,
        "user_name": "test",
        "user_email": "test@email.com",
        "user_age": null,
        "user_gender": null,
        "user_height": null,
        "user_weight": null
    }
  }
  ```
