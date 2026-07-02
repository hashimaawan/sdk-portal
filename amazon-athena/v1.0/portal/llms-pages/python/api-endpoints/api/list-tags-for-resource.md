# List Tags for Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRkxpc3RUYWdzRm9yUmVzb3VyY2U

Lists the tags associated with an Athena workgroup or data catalog resource.

```python
def list_tags_for_resource(self,
                          x_amz_target,
                          body,
                          x_amz_content_sha_256=None,
                          x_amz_date=None,
                          x_amz_algorithm=None,
                          x_amz_credential=None,
                          x_amz_security_token=None,
                          x_amz_signature=None,
                          x_amz_signed_headers=None,
                          max_results=None,
                          next_token=None)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `x_amz_target` | [`XAmzTarget44`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-44.md) | Header, Required | - |
| `body` | [`ListTagsForResourceInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/list-tags-for-resource-input.md) | Body, Required | - |
| `x_amz_content_sha_256` | `str` | Header, Optional | - |
| `x_amz_date` | `str` | Header, Optional | - |
| `x_amz_algorithm` | `str` | Header, Optional | - |
| `x_amz_credential` | `str` | Header, Optional | - |
| `x_amz_security_token` | `str` | Header, Optional | - |
| `x_amz_signature` | `str` | Header, Optional | - |
| `x_amz_signed_headers` | `str` | Header, Optional | - |
| `max_results` | `str` | Query, Optional | Pagination limit |
| `next_token` | `str` | Query, Optional | Pagination token |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ListTagsForResourceOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/list-tags-for-resource-output.md).


# Example Usage

```python
x_amz_target = XAmzTarget44.ENUM_AMAZONATHENALISTTAGSFORRESOURCE

body = ListTagsForResourceInput(
    resource_arn='ResourceARN4'
)

result = client_api.list_tags_for_resource(
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



