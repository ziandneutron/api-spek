## Register

### Request
- Enpoint : `POST` /auth/register
- Body : 

    ```
    {
        email: "user@test.local",
        password: "123123",
        name: "User Test"
    }
    ```

### Response
- Status : `201`

    ```
    {
        token: {
            accessToken: "kshdjhisah829r745dsfhsjkdhfdsf",
            refreshToken: "kshdjhisah829r745dsfhsjk123dsf"
        } 
        user: {
            email: "user@test.local",
            name: "User Test"
        }
    }
    ```

---

## Login

### Request
- Enpoint : `POST` /auth/login
- Body : 

    ```
    {
        email: "user@test.local",
        password: "123123"
    }
    ```

### Response
- Status : `200`

    ```
    {
        token: {
            accessToken: "kshdjhisah829r745dsfhsjkdhfdsf",
            refreshToken: "kshdjhisah829r745dsfhsjk123dsf"
        } 
        user: {
            email: "user@test.local",
            name: "User Test"
        }
    }
    ```
### Response Failed
- Status : `401`

    ```
    {
        message: "unauthorized"
    }
    ```
---


## User

### Request
- Enpoint : `GET` /auth/user
- Headers :
    ```
    {
        Authorization: "Bearer kshdjhisah829r745dsfhsjkdhfdsf"
    }
    ```

### Response Success
- Status : `200`

    ```
    {
        email: "user@test.local",
        name: "User Test"
    }
    ```

### Response Failed
- Status : `401`

    ```
    {
        message: "unauthorized"
    }
    ```