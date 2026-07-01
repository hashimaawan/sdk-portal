# Retry Issuance or Renewal

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRkNlcnRpZmljYXRlJTI1MjBBY3Rpb25zJTJGUmV0cnklMjUyMElzc3VhbmNlJTI1MjBvciUyNTIwUmVuZXdhbA

Retry a failed Certificate issuance or renewal.

Only applicable if the type of the Certificate is `managed` and the issuance or renewal status is `failed`.

#### Call specific error codes

| Code                                                    | Description                                                               |
|---------------------------------------------------------|---------------------------------------------------------------------------|
| `caa_record_does_not_allow_ca`                          | CAA record does not allow certificate authority                           |
| `ca_dns_validation_failed`                              | Certificate Authority: DNS validation failed                              |
| `ca_too_many_authorizations_failed_recently`            | Certificate Authority: Too many authorizations failed recently            |
| `ca_too_many_certificates_issued_for_registered_domain` | Certificate Authority: Too many certificates issued for registered domain |
| `ca_too_many_duplicate_certificates`                    | Certificate Authority: Too many duplicate certificates                    |
| `could_not_verify_domain_delegated_to_zone`             | Could not verify domain delegated to zone                                 |
| `dns_zone_not_found`                                    | DNS zone not found                                                        |
| `dns_zone_is_secondary_zone`                            | DNS zone is a secondary zone                                              |

:information_source: **Note** This endpoint does not require authentication.

```ts
async retryIssuanceOrRenewal(
  id: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ActionResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Certificate |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**201**: The `action` key contains the resulting Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action-response.md).


# Example Usage

```ts
const id = 112;

try {
  const response = await certificateActionsApi.retryIssuanceOrRenewal(id);

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "issue_certificate",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": "2021-01-30T23:57:00+00:00",
    "id": 14,
    "progress": 100,
    "resources": [
      {
        "id": 896,
        "type": "certificate"
      }
    ],
    "started": "2021-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



