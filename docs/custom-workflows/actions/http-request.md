# Action: send HTTP request

This action will transmit an HTTP request to a given URL. This is especially useful when integrating with third-party services in which there is a need to transmit content to an external API or service. 

!!! info "Limitations"
    Currently, this action does not parse the response or make the contents of the response available to subsequent actions. Therefore, it may be difficult to detect and respond to errors.

## Input

| Variable         | Type     | Description                                                         |
|------------------|----------|---------------------------------------------------------------------|
| **URL**          | URL      | The URL to make the HTTP request to.                                |
| **Method**       | String   | The HTTP method of the request. Supports GET, PUT, POST and DELETE. |
| **Content-type** | String   | The content-type of the request.                                    |
| **Request body** | String   | The body of the request, used in POST requests.                     |
| **Headers**      | KeyValue | The HTTP headers of the request.                                    |

!!! info "Info"
    When URL is set to endpoint of [RingCentral APIs](https://developers.ringcentral.com/api-reference/) (domain: https://platform.ringcentral.com), the Authorization header will be set with the automations's runner's token automatically.

## Output

None.
