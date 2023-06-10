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
