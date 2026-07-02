# ApiException

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0aCUyRl9fYWRkaXRpb25hbF9kb2N1bWVudGF0aW9uJTJGVXRpbGl0aWVzJTJGQXBpRXhjZXB0aW9u

Thrown when there is a network error or HTTP response status code is not okay. It also extends [Exception](https://www.php.net/manual/en/class.exception.php) that provides it with methods like `getMessage()`, `getCode()`, etc.

# Methods

| Name | Type | Description |
|  --- | --- | --- |
| `getHttpRequest()` | [`HttpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/sdk-infrastructure/http/httprequest.md) | Returns the HTTP request. |
| `getHttpResponse()` | [`?HttpResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/sdk-infrastructure/http/httpresponse.md) | Returns the HTTP response. |
| `hasResponse()` | `bool` | Is the response available? |



