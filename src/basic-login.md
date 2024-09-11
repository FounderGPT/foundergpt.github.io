# Sign In

Log in to the FounderGPT API using email and password.

-   Takes a username and password, and returns a token that can be used to authenticate future requests like querying FounderGPT and setting up third-party integrations.

_Note: to sign up, please contact us at gptfounder@gmail.com as the app is currently invite only._

### Endpoint

-   Method: `POST`
-   URL: `app.foundergpt.com/login`
-   Authentication: No, not required

### Request

-   Type: `JSON`
-   Fields:
    -   `email`
        -   type: `string`
        -   description: The email of the user.
    -   `password`
        -   type: `string`
        -   description: The password of the user.

### Response

-   Type: `JSON`
-   Fields:
    -   `success`
        -   type: `boolean`
        -   description: Whether the login was successful.
    -   `response`
        -   type: `string`
        -   description: Message regarding login success or failure.
    -   `error`
        -   type: `string`
        -   description: Error details if any error occurs or login fails.
    -   `user_id`
        -   type: `string` (UUID)
        -   description: The user ID of the user.
    -   `token`
        -   type: `string` (JWT Token)
        -   description: The token for the user. Save this token for future requests. Needs to be passed into the API endpoints that require authentication.
