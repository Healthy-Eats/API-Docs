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
  
  Value = Bearer (token from login)

- Response
  ```json
  {
    "status": "success",
    "message": "read successful",
    "data": {
        "user_id": (user id),
        "user_name": "test",
        "user_email": "test@email.com",
        "user_age": null,
        "user_gender": null,
        "user_height": null,
        "user_weight": null
    }
  }
  ```

### Update User
- Method

  PUT

- URL

  /updateUser

- Headers

  Key = Authorization
  
  Value = Bearer (token from login)

- Body Request
  ```json
  {
    "name": "test",
    "age": 21,
    "gender": "MALE",
    "height": 200,
    "weight": 100
  }
  ```

- Response
  ```json
  {
      "status": "success",
      "message": "update successful"
  }
  ```

### Delete User
- Method

  DELETE

- URL

  /deleteUser

- Headers

  Key = Authorization
  
  Value = Bearer (token from login)

- Response
  ```json
  {
      "status": "success",
      "message": "Delete successful"
  }
  ```

### Create Plan
- Method

  POST

- URL

  /createPlan

- Headers

  Key = Authorization
  
  Value = Bearer (token from login)

- Body Request
  ```json
  {
    "name": "deficit calorie",
    "goal": "decrease body weight",
    "activity": "Active",
    "calories_target": 1500
  }
  ```

- Response
  ```json
  {
      "status": "success",
      "message": "Plan created successfully"
  }
  ```

### Read Plan
- Method

  GET

- URL

  /readPlan

- Headers

  Key = Authorization
  
  Value = Bearer (token from login)

- Response
  ```json
  {
      "status": "success",
      "message": "read successful",
      "data": {
          "plan": {
              "plan_id": (plan id),
              "plan_name": "deficit calorie",
              "plan_goal": "decrease body weight",
              "plan_activity": "Active",
              "calories_target": 1500,
              "calories_consume": 0,
              "user_id": (user id)
          }
      }
  }
  ```
