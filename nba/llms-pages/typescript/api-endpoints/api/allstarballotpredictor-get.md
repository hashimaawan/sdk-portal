# Allstarballotpredictor GET

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/#/typescript/x-redirect/JTI0ZSUyRiUyRkFsbHN0YXJiYWxsb3RwcmVkaWN0b3JfR0VU

:information_source: **Note** This endpoint does not require authentication.

```ts
async allstarballotpredictorGET(
  westPlayer1: string,
  westPlayer2: string,
  westPlayer3: string,
  westPlayer4: string,
  westPlayer5: string,
  eastPlayer1: string,
  eastPlayer2: string,
  eastPlayer3: string,
  eastPlayer4: string,
  eastPlayer5: string,
  pointCap?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `westPlayer1` | `string` | Query, Required | - |
| `westPlayer2` | `string` | Query, Required | - |
| `westPlayer3` | `string` | Query, Required | - |
| `westPlayer4` | `string` | Query, Required | - |
| `westPlayer5` | `string` | Query, Required | - |
| `eastPlayer1` | `string` | Query, Required | - |
| `eastPlayer2` | `string` | Query, Required | - |
| `eastPlayer3` | `string` | Query, Required | - |
| `eastPlayer4` | `string` | Query, Required | - |
| `eastPlayer5` | `string` | Query, Required | - |
| `pointCap` | `string \| undefined` | Query, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: 200 OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/nba/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const westPlayer1 = 'WestPlayer10';

const westPlayer2 = 'WestPlayer24';

const westPlayer3 = 'WestPlayer32';

const westPlayer4 = 'WestPlayer48';

const westPlayer5 = 'WestPlayer56';

const eastPlayer1 = 'EastPlayer18';

const eastPlayer2 = 'EastPlayer26';

const eastPlayer3 = 'EastPlayer32';

const eastPlayer4 = 'EastPlayer44';

const eastPlayer5 = 'EastPlayer54';

try {
  const response = await apiController.allstarballotpredictorGET(
    westPlayer1,
    westPlayer2,
    westPlayer3,
    westPlayer4,
    westPlayer5,
    eastPlayer1,
    eastPlayer2,
    eastPlayer3,
    eastPlayer4,
    eastPlayer5
  );

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


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request - bad parameters | `ApiError` |
| 404 | 'No HTTP resource was found that matches the request URI' - possible deprecated endpoint | `ApiError` |



