# Action: send HTTP request

This action will transmit an HTTP request to a given URL. This is especially useful when integrating with third-party services in which there is a need to transmit content to an external API or service. 

!!! info "Limitations"
    Currently, this action does not parse the response or make the contents of the response available to subsequent actions. Therefore, it may be difficult to detect and respond to errors.

## Input

| Variable         | Type     | Description                                                                |
|------------------|----------|----------------------------------------------------------------------------|
| **URL**          | URL      | The URL to make the HTTP request to.                                       |
| **Method**       | String   | The HTTP method of the request. Supports GET, POST, PUT, PATCH and DELETE. |
| **Content-type** | String   | The content-type of the request.                                           |
| **Request body** | String   | The body of the request, used in POST, PUT, PATCH and DELETE requests.     |
| **Headers**      | KeyValue | The HTTP headers of the request.                                           |

!!! hint "Authenticating with RingCentral APIs"
    When the HTTP request action is used to call a [RingCentral API](https://developers.ringcentral.com/api-reference/), which we detect by looking at the hostname of the URL, the request's `Authorization` header will be set for you automatically using the automation runner's access token.

## Output

None.
