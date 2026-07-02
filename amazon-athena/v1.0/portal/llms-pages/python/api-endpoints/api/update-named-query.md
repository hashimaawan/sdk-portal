# Update Named Query

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRlVwZGF0ZU5hbWVkUXVlcnk

Updates a <a>NamedQuery</a> object. The database or workgroup cannot be updated.

```python
def update_named_query(self,
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
| `x_amz_target` | [`XAmzTarget55Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-55.md) | Header, Required | - |
| `body` | [`UpdateNamedQueryInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/update-named-query-input.md) | Body, Required | - |
| `x_amz_content_sha_256` | `str` | Header, Optional | - |
| `x_amz_date` | `str` | Header, Optional | - |
| `x_amz_algorithm` | `str` | Header, Optional | - |
| `x_amz_credential` | `str` | Header, Optional | - |
| `x_amz_security_token` | `str` | Header, Optional | - |
| `x_amz_signature` | `str` | Header, Optional | - |
| `x_amz_signed_headers` | `str` | Header, Optional | - |


# Response Type

**200**: Success

`Any`


# Example Usage

```python
x_amz_target = XAmzTarget55Enum.ENUM_AMAZONATHENAUPDATENAMEDQUERY

body = UpdateNamedQueryInput(
    named_query_id='NamedQueryId6',
    name='Name6',
    query_string='QueryString8'
)

result = client_controller.update_named_query(
    x_amz_target,
    body
)
print(result)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `APIException` |
| 481 | InvalidRequestException | `APIException` |



