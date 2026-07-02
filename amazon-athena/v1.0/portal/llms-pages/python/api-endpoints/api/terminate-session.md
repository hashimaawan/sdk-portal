# Terminate Session

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRlRlcm1pbmF0ZVNlc3Npb24

Terminates an active session. A <code>TerminateSession</code> call on a session that is already inactive (for example, in a <code>FAILED</code>, <code>TERMINATED</code> or <code>TERMINATING</code> state) succeeds but has no effect. Calculations running in the session when <code>TerminateSession</code> is called are forcefully stopped, but may display as <code>FAILED</code> instead of <code>STOPPED</code>.

```python
def terminate_session(self,
                     x_amz_target,
                     body,
                     x_amz_content_sha_256=None,
                     x_amz_date=None,
                     x_amz_algorithm=None,
                     x_amz_credential=None,
                     x_amz_security_token=None,
                     x_amz_signature=None,
                     x_amz_signed_headers=None)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `x_amz_target` | [`XAmzTarget52`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-52.md) | Header, Required | - |
| `body` | [`TerminateSessionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/terminate-session-request.md) | Body, Required | - |
| `x_amz_content_sha_256` | `str` | Header, Optional | - |
| `x_amz_date` | `str` | Header, Optional | - |
| `x_amz_algorithm` | `str` | Header, Optional | - |
| `x_amz_credential` | `str` | Header, Optional | - |
| `x_amz_security_token` | `str` | Header, Optional | - |
| `x_amz_signature` | `str` | Header, Optional | - |
| `x_amz_signed_headers` | `str` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`TerminateSessionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/terminate-session-response.md).


# Example Usage

```python
x_amz_target = XAmzTarget52.ENUM_AMAZONATHENATERMINATESESSION

body = TerminateSessionRequest(
    session_id='SessionId2'
)

result = client_api.terminate_session(
    x_amz_target,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `ApiException` |
| 481 | InvalidRequestException | `ApiException` |
| 482 | ResourceNotFoundException | `ApiException` |



