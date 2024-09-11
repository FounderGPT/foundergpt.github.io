# Ask Questions

Ask FounderGPT to provide information or complete a task.

-   Takes a query and returns a response from FounderGPT, after FounderGPT has gathered the information or completed the requested task.

### Endpoint

-   Method: `POST`
-   URL: `app.foundergpt.com/query`
-   Authentication: Yes, required
    -   Provide the token (obtained from the sign-in endpoint) in the `Authorization` HTTP header, with typical Bearer token format.

### Request

-   Type: `JSON`
-   Fields:
    -   `query`
        -   type: `string`
        -   description: A natural language question, request for information, or request to complete a task.
    -   `current_time`
        -   type: `string`
        -   description: The current time including timezone, in RFC3339 format or this format: `yyyy-MM-dd'T'HH:mm:ssZZZZZ`

### Response

-   Type: `JSON`
-   Fields:
    -   `success`
        -   type: `boolean`
        -   description: Whether the query was successful.
    -   `response`
        -   type: `string`
        -   description: Response from the chatbot, intended to be displayed to the user.
    -   `error`
        -   type: `string`
        -   description: Error details if any error occurs or query fails.
    -   `query`
        -   type: `string`
        -   description: The original query provided in the request.
