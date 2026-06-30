# Getting Started

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/go/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Furkot provides Rest API to access user trip data.
Using Furkot API an application can list user trips and display stops for a specific trip.
Furkot API uses OAuth2 protocol to authorize applications to access data on behalf of users.

Furkot API description: [https://help.furkot.com/widgets/furkot-api.html](https://help.furkot.com/widgets/furkot-api.html)

## Requirements

The SDK requires **Go version 1.18 or above**.


# Building

## Install Dependencies

Resolve all the SDK dependencies, using the `go get` command.


# Installation

The following section explains how to use the furkottrips library in a new project.

## 1. Add SDK as a Dependency to the Application

- Add the following lines to your application's `go.mod` file:

```go
replace furkottrips => ".\\Random Directory" // local path to the SDK

require furkottrips v0.0.0
```

- Resolve the dependencies in the updated `go.mod` file, using the `go get` command.


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/go/getting-started/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpConfiguration | [`HttpConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/go/sdk-infrastructure/configuration/httpconfiguration.md) | Configurable http client options like timeout and retries. |
| furkotAuthAccessCodeCredentials | [`FurkotAuthAccessCodeCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/go/getting-started/authorization.md) | The Credentials Setter for OAuth 2 Authorization Code Grant |
| furkotAuthImplicitCredentials | [`FurkotAuthImplicitCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/go/getting-started/authorization.md) | The Credentials Setter for OAuth 2 Implicit Grant |

The API client can be initialized as follows:

```go
package main

import (
    "furkottrips"
    "furkottrips/models"
)

func main() {
    client := furkottrips.NewClient(
    furkottrips.CreateConfiguration(
            furkottrips.WithHttpConfiguration(
                furkottrips.CreateHttpConfiguration(
                    furkottrips.WithTimeout(0),
                ),
            ),
            furkottrips.WithEnvironment(furkottrips.PRODUCTION),
            furkottrips.WithFurkotAuthAccessCodeCredentials(
                furkottrips.NewFurkotAuthAccessCodeCredentials(
                    "OAuthClientId",
                    "OAuthClientSecret",
                    "OAuthRedirectUri",
                ).
                WithOAuthScopes([]models.OAuthScopeFurkotAuthAccessCodeEnum{
        models.OAuthScopeFurkotAuthAccessCodeEnum_READTRIPS,
    }),
            ),
            furkottrips.WithFurkotAuthImplicitCredentials(
                furkottrips.NewFurkotAuthImplicitCredentials(
                    "OAuthClientId",
                    "OAuthRedirectUri",
                ).
                WithOAuthScopes([]models.OAuthScopeFurkotAuthImplicitEnum{
        models.OAuthScopeFurkotAuthImplicitEnum_READTRIPS,
    }),
            ),
        ),
    )
}
```


# Authorization

This API uses the following authentication schemes.

* [`furkot_auth_access_code (OAuth 2 Authorization Code Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/go/getting-started/authorization.md)
* [`furkot_auth_implicit (OAuth 2 Implicit Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/go/getting-started/authorization.md)

## furkot_auth_access_code (OAuth 2 Authorization Code Grant)



Documentation for accessing and setting credentials for furkot_auth_access_code.

### Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| oAuthClientId | `string` | OAuth 2 Client ID | `WithOAuthClientId` | `OAuthClientId()` |
| oAuthClientSecret | `string` | OAuth 2 Client Secret | `WithOAuthClientSecret` | `OAuthClientSecret()` |
| oAuthRedirectUri | `string` | OAuth 2 Redirection endpoint or Callback Uri | `WithOAuthRedirectUri` | `OAuthRedirectUri()` |
| oAuthToken | `OAuthToken` | Object for storing information about the OAuth token | `WithOAuthToken` | `OAuthToken()` |
| oAuthScopes | `[]OAuthScopeFurkotAuthAccessCodeEnum` | List of scopes that apply to the OAuth token | `WithOAuthScopes` | `OAuthScopes()` |



**Note:** Required auth credentials can be set using `WithFurkotAuthAccessCodeCredentials()` by providing a credentials instance with `NewFurkotAuthAccessCodeCredentials()` in the configuration initialization and accessed using the `FurkotAuthAccessCodeCredentials()` method in the configuration instance.

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```go
package main

import (
    "furkottrips"
    "furkottrips/models"
)

func main() {
    client := furkottrips.NewClient(
    furkottrips.CreateConfiguration(
            furkottrips.WithFurkotAuthAccessCodeCredentials(
                furkottrips.NewFurkotAuthAccessCodeCredentials(
                    "OAuthClientId",
                    "OAuthClientSecret",
                    "OAuthRedirectUri",
                ).
                WithOAuthScopes([]models.OAuthScopeFurkotAuthAccessCodeEnum{
        models.OAuthScopeFurkotAuthAccessCodeEnum_READTRIPS,
    }),
            ),
        ),
    )
}
```



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Authorization Code Grant*. This authorization includes the following steps

### 2\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page.The `BuildAuthorizationURL` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```go
state := "session-state"
url := client.FurkotAuthAccessCodeManager().BuildAuthorizationURL(state)
// redirect the user to the given URL and get a code after the user consents
```

### 3\. Handle the OAuth server response

Once the user responds to the consent request, the OAuth 2.0 server responds to your application's access request by redirecting the user to the redirect URI specified set in `Configuration`.

If the user approves the request, the authorization code will be sent as the `code` query string:

```
https://example.com/oauth/callback?code=XXXXXXXXXXXXXXXXXXXXXXXXX
```

If the user does not approve the request, the response contains an `error` query string:

```
https://example.com/oauth/callback?error=access_denied
```

### 4\. Authorize the client using the code

After the server receives the code, it can exchange this for an *access token*. The access token is an object containing information for authorizing client requests and refreshing the token itself.

```go
oAuthToken, err := client.FurkotAuthAccessCodeManager().FetchToken(ctx, authCode)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the token
    fmt.Println(oAuthToken)
}

// Creating a new client with the token
client = client.CloneWithConfiguration(
    furkottrips.WithFurkotAuthAccessCodeCredentials(
        client.Configuration().FurkotAuthAccessCodeCredentials().
            WithOAuthToken(oAuthToken),
    ),
)
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeFurkotAuthAccessCodeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/go/models/enumerations/o-auth-scope-furkot-auth-access-code.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list trips and stops info |

### Refreshing the token

An access token may expire after sometime. To extend its lifetime, you must refresh the token.

```go
if client.FurkotAuthAccessCodeManager().OAuthTokenIsExpired() {
    oAuthToken, err := client.FurkotAuthAccessCodeManager().RefreshToken(ctx)
    if err != nil {
        log.Fatalln(err)
    } else {
        // Printing the token
        fmt.Println(oAuthToken)
    }

    // Creating a new client with the token
    client = client.CloneWithConfiguration(
        furkottrips.WithFurkotAuthAccessCodeCredentials(
            client.Configuration().FurkotAuthAccessCodeCredentials().
                WithOAuthToken(oAuthToken),
        ),
    )
}
```

If a token expires, an error will be returned before the next endpoint call requiring authentication.

### Storing an access token for reuse

It is recommended that you store the access token for reuse.

```go
oAuthToken := client.Configuration().FurkotAuthAccessCodeCredentials().OAuthToken()
StoreInDatabase(oAuthToken)
```

### Creating a client from a stored token

To authorize a client using a stored access token, just set the access token in Configuration along with the other configuration parameters before creating the client:

```go
// Get token from storage
oAuthToken := GetStoredToken()

// Creating a new client with the token
client = client.CloneWithConfiguration(
    furkottrips.WithFurkotAuthAccessCodeCredentials(
        client.Configuration().FurkotAuthAccessCodeCredentials().
            WithOAuthToken(oAuthToken),
    ),
)
```

### Complete example



```go
package main

import (
    "context"
    "fmt"
    "furkottrips"
    "furkottrips/models"
    "log"
)

func main() {
    ctx := context.Background()
    
    // Client configuration
    package main
    import (
        "furkottrips"
        "furkottrips/models"
    )
    func main() {
        client := furkottrips.NewClient(
        furkottrips.CreateConfiguration(
                furkottrips.WithFurkotAuthAccessCodeCredentials(
                    furkottrips.NewFurkotAuthAccessCodeCredentials(
                        "OAuthClientId",
                        "OAuthClientSecret",
                        "OAuthRedirectUri",
                    ).
                    WithOAuthScopes([]models.OAuthScopeFurkotAuthAccessCodeEnum{
            models.OAuthScopeFurkotAuthAccessCodeEnum_READTRIPS,
        }),
                ),
            ),
        )
    }
    
    // Obtain access token, restore from cache if possible
    if oAuthToken, err := GetStoredToken(); err == nil {
        // Refresh the token if it is expired
        if client.FurkotAuthAccessCodeManager().OAuthTokenIsExpired() {
            oAuthToken, err = client.FurkotAuthAccessCodeManager().RefreshToken(ctx)
            if err != nil {
                log.Fatalln(err)
            } else {
                // Printing the token
                fmt.Println(oAuthToken)
            }
        }
        
        // Creating a new client with the token
        client = client.CloneWithConfiguration(
            furkottrips.WithFurkotAuthAccessCodeCredentials(
                client.Configuration().FurkotAuthAccessCodeCredentials().
                    WithOAuthToken(oAuthToken),
            ),
        )
    } else {
        // build authorization url to redirect the user
        state := "session-state"
        url := client.FurkotAuthAccessCodeManager().BuildAuthorizationURL(state)
        // redirect the user to the given URL and get a code after the user consents
        authCode := GetAuthCode(url)
        
        // Fetch an access token to authorize the client
        oAuthToken, err := client.FurkotAuthAccessCodeManager().FetchToken(ctx, authCode)
        if err != nil {
            log.Fatalln(err)
        } else {
            // Printing the token
            fmt.Println(oAuthToken)
        }
        
        // Creating a new client with the token
        client = client.CloneWithConfiguration(
            furkottrips.WithFurkotAuthAccessCodeCredentials(
                client.Configuration().FurkotAuthAccessCodeCredentials().
                    WithOAuthToken(oAuthToken),
            ),
        )
        
        // Store the token
        StoreInDatabase(oAuthToken)
    }
    
    // The client is now authorized; you can use the client to make endpoint calls
}

func GetStoredToken() (
    models.OAuthToken,
    error) {
    // Get token logic here
    return models.OAuthToken{}, nil
}

func StoreInDatabase(oAuthToken models.OAuthToken) {
    // Save token logic here
}

func GetAuthCode(redirectURL string) string {
    // User redirection logic here
    return ""
}
```

## furkot_auth_implicit (OAuth 2 Implicit Grant)



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Implicit Grant* to obtain a user's consent to perform an API request on user's behalf. This authorization includes the following steps

This process requires the presence of a client-side JavaScript code on the redirect URI page to receive the *access token* after the consent step is completed.

### 1\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page. The `BuildAuthorizationURL` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```go
state := "session-state"
url := client.FurkotAuthImplicitManager().BuildAuthorizationURL(state)
// redirect the user to the given URL and get a code after the user consents
```

### 2\. Handle the OAuth server response

Once the user responds to the consent request, the OAuth 2.0 server responds to your application's access request by redirecting the user to the redirect URI specified set in `Configuration`.

The redirect URI will receive the *access token* as the `token` argument in the URL fragment.

```
https://example.com/oauth/callback#token=XXXXXXXXXXXXXXXXXXXXXXXXX
```

The access token must be extracted by the client-side JavaScript code. The access token can be used to authorize any further endpoint calls by the JavaScript code.

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeFurkotAuthImplicitEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/go/models/enumerations/o-auth-scope-furkot-auth-implicit.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list users trips info |




