# Quickstart

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

You can use Spotify's Web API to discover music and podcasts, manage your Spotify library, control audio playback, and much more. Browse our available Web API endpoints using the sidebar at left, or via the navigation bar on top of this page on smaller screens.

In order to make successful Web API requests your app will need a valid access token. One can be obtained through <a href="https://developer.spotify.com/documentation/general/guides/authorization-guide/">OAuth 2.0</a>.

The base URI for all Web API requests is `https://api.spotify.com/v1`.

Need help? See our <a href="https://developer.spotify.com/documentation/web-api/guides/">Web API guides</a> for more information, or visit the <a href="https://community.spotify.com/t5/Spotify-for-Developers/bd-p/Spotify_Developer">Spotify for Developers community forum</a> to ask questions and connect with other developers.

## Requirements

The SDK requires **Go version 1.18 or above**.


# Building

## Install Dependencies

Resolve all the SDK dependencies, using the `go get` command.


# Installation

The following section explains how to use the spotifyWebApiWithFixesAndImprovementsFromSonallux library in a new project.

## 1. Add SDK as a Dependency to the Application

- Add the following lines to your application's `go.mod` file:

```go
replace spotifyWebApiWithFixesAndImprovementsFromSonallux => ".\\Random Directory" // local path to the SDK

require spotifyWebApiWithFixesAndImprovementsFromSonallux v0.0.0
```

- Resolve the dependencies in the updated `go.mod` file, using the `go get` command.


# Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

## Fields

| Name | Description |
|  --- | --- |
| Production | **Default** |


# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/getting-started/quickstart/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpConfiguration | [`HttpConfiguration`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/sdk-infrastructure/configuration/httpconfiguration.md) | Configurable http client options like timeout and retries. |
| loggerConfiguration | [`LoggerConfiguration`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/sdk-infrastructure/configuration/loggerconfiguration.md) | Represents the logger configurations for API calls |
| authorizationCodeAuth | [`AuthorizationCodeAuth`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/getting-started/quickstart/authorization.md) | The Credentials Setter for OAuth 2 Authorization Code Grant |

The API client can be initialized as follows:

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux"
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    client := spotifyWebApiWithFixesAndImprovementsFromSonallux.NewClient(
    spotifyWebApiWithFixesAndImprovementsFromSonallux.CreateConfiguration(
            spotifyWebApiWithFixesAndImprovementsFromSonallux.WithHttpConfiguration(
                spotifyWebApiWithFixesAndImprovementsFromSonallux.CreateHttpConfiguration(
                    spotifyWebApiWithFixesAndImprovementsFromSonallux.WithTimeout(30),
                ),
            ),
            spotifyWebApiWithFixesAndImprovementsFromSonallux.WithEnvironment(spotifyWebApiWithFixesAndImprovementsFromSonallux.PRODUCTION),
            spotifyWebApiWithFixesAndImprovementsFromSonallux.WithAuthorizationCodeAuthCredentials(
                spotifyWebApiWithFixesAndImprovementsFromSonallux.NewAuthorizationCodeAuthCredentials(
                    "OAuthClientId",
                    "OAuthClientSecret",
                    "OAuthRedirectUri",
                ).
                WithOauthScopes([]models.OauthScope{
        models.OauthScope_AppRemoteControl,
        models.OauthScope_PlaylistReadPrivate,
    }),
            ),
            spotifyWebApiWithFixesAndImprovementsFromSonallux.WithLoggerConfiguration(
                spotifyWebApiWithFixesAndImprovementsFromSonallux.WithLevel("info"),
                spotifyWebApiWithFixesAndImprovementsFromSonallux.WithRequestConfiguration(
                    spotifyWebApiWithFixesAndImprovementsFromSonallux.WithRequestBody(true),
                ),
                spotifyWebApiWithFixesAndImprovementsFromSonallux.WithResponseConfiguration(
                    spotifyWebApiWithFixesAndImprovementsFromSonallux.WithResponseHeaders(true),
                ),
            ),
        ),
    )
}
```


# Authorization

This API uses the following authentication schemes.

* [`oauth_2_0 (OAuth 2 Authorization Code Grant)`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/getting-started/quickstart/authorization.md)

## oauth_2_0 (OAuth 2 Authorization Code Grant)



Documentation for accessing and setting credentials for oauth_2_0.

### Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| oauthClientId | `string` | OAuth 2 Client ID | `WithOauthClientId` | `OauthClientId()` |
| oauthClientSecret | `string` | OAuth 2 Client Secret | `WithOauthClientSecret` | `OauthClientSecret()` |
| oauthRedirectUri | `string` | OAuth 2 Redirection endpoint or Callback Uri | `WithOauthRedirectUri` | `OauthRedirectUri()` |
| oauthToken | `OauthToken` | Object for storing information about the OAuth token | `WithOauthToken` | `OauthToken()` |
| oauthScopes | `[]OauthScope` | List of scopes that apply to the OAuth token | `WithOauthScopes` | `OauthScopes()` |



**Note:** Required auth credentials can be set using `WithAuthorizationCodeAuth()` by providing a credentials instance with `NewAuthorizationCodeAuth()` in the configuration initialization and accessed using the `AuthorizationCodeAuth()` method in the configuration instance.

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux"
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    client := spotifyWebApiWithFixesAndImprovementsFromSonallux.NewClient(
    spotifyWebApiWithFixesAndImprovementsFromSonallux.CreateConfiguration(
            spotifyWebApiWithFixesAndImprovementsFromSonallux.WithAuthorizationCodeAuthCredentials(
                spotifyWebApiWithFixesAndImprovementsFromSonallux.NewAuthorizationCodeAuthCredentials(
                    "OAuthClientId",
                    "OAuthClientSecret",
                    "OAuthRedirectUri",
                ).
                WithOauthScopes([]models.OauthScope{
        models.OauthScope_AppRemoteControl,
        models.OauthScope_PlaylistReadPrivate,
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
url := client.AuthorizationCodeAuthManager().BuildAuthorizationURL(state)
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
oauthToken, err := client.AuthorizationCodeAuthManager().FetchToken(ctx, authCode)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the token
    fmt.Println(oauthToken)
}

// Creating a new client with the token
client = client.CloneWithConfiguration(
    spotifyWebApiWithFixesAndImprovementsFromSonallux.WithAuthorizationCodeAuthCredentials(
        client.Configuration().AuthorizationCodeAuthCredentials().
            WithOAuthToken(oauthToken),
    ),
)
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OauthScope`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/enumerations/oauth-scope.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `APP_REMOTE_CONTROL` | Communicate with the Spotify app on your device. |
| `PLAYLIST_READ_PRIVATE` | Access your private playlists. |
| `PLAYLIST_READ_COLLABORATIVE` | Access your collaborative playlists. |
| `PLAYLIST_MODIFY_PUBLIC` | Manage your public playlists. |
| `PLAYLIST_MODIFY_PRIVATE` | Manage your private playlists. |
| `USER_LIBRARY_READ` | Access your saved content. |
| `USER_LIBRARY_MODIFY` | Manage your saved content. |
| `USER_READ_PRIVATE` | Access your subscription details. |
| `USER_READ_EMAIL` | Get your real email address. |
| `USER_FOLLOW_READ` | Access your followers and who you are following. |
| `USER_FOLLOW_MODIFY` | Manage your saved content. |
| `USER_TOP_READ` | Read your top artists and content. |
| `USER_READ_PLAYBACK_POSITION` | Read your position in content you have played. |
| `USER_READ_PLAYBACK_STATE` | Read your currently playing content and Spotify Connect devices information. |
| `USER_READ_RECENTLY_PLAYED` | Access your recently played items. |
| `USER_READ_CURRENTLY_PLAYING` | Read your currently playing content. |
| `USER_MODIFY_PLAYBACK_STATE` | Control playback on your Spotify clients and Spotify Connect devices. |
| `UGC_IMAGE_UPLOAD` | Upload images to Spotify on your behalf. |
| `STREAMING` | Play content and control playback on your other devices. |

### Refreshing the token

An access token may expire after sometime. To extend its lifetime, you must refresh the token.

```go
if client.AuthorizationCodeAuthManager().OAuthTokenIsExpired() {
    oauthToken, err := client.AuthorizationCodeAuthManager().RefreshToken(ctx)
    if err != nil {
        log.Fatalln(err)
    } else {
        // Printing the token
        fmt.Println(oauthToken)
    }

    // Creating a new client with the token
    client = client.CloneWithConfiguration(
        spotifyWebApiWithFixesAndImprovementsFromSonallux.WithAuthorizationCodeAuthCredentials(
            client.Configuration().AuthorizationCodeAuthCredentials().
                WithOAuthToken(oauthToken),
        ),
    )
}
```

If a token expires, an error will be returned before the next endpoint call requiring authentication.

### Storing an access token for reuse

It is recommended that you store the access token for reuse.

```go
oauthToken := client.Configuration().AuthorizationCodeAuthCredentials().OAuthToken()
StoreInDatabase(oauthToken)
```

### Creating a client from a stored token

To authorize a client using a stored access token, just set the access token in Configuration along with the other configuration parameters before creating the client:

```go
// Get token from storage
oauthToken := GetStoredToken()

// Creating a new client with the token
client = client.CloneWithConfiguration(
    spotifyWebApiWithFixesAndImprovementsFromSonallux.WithAuthorizationCodeAuthCredentials(
        client.Configuration().AuthorizationCodeAuthCredentials().
            WithOAuthToken(oauthToken),
    ),
)
```

### Complete example



```go
package main

import (
    "context"
    "fmt"
    "log"
    "spotifyWebApiWithFixesAndImprovementsFromSonallux"
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    ctx := context.Background()
    
    // Client configuration
    package main
    import (
        "spotifyWebApiWithFixesAndImprovementsFromSonallux"
        "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
    )
    func main() {
        client := spotifyWebApiWithFixesAndImprovementsFromSonallux.NewClient(
        spotifyWebApiWithFixesAndImprovementsFromSonallux.CreateConfiguration(
                spotifyWebApiWithFixesAndImprovementsFromSonallux.WithAuthorizationCodeAuthCredentials(
                    spotifyWebApiWithFixesAndImprovementsFromSonallux.NewAuthorizationCodeAuthCredentials(
                        "OAuthClientId",
                        "OAuthClientSecret",
                        "OAuthRedirectUri",
                    ).
                    WithOauthScopes([]models.OauthScope{
            models.OauthScope_AppRemoteControl,
            models.OauthScope_PlaylistReadPrivate,
        }),
                ),
            ),
        )
    }
    
    // Obtain access token, restore from cache if possible
    if oauthToken, err := GetStoredToken(); err == nil {
        // Refresh the token if it is expired
        if client.AuthorizationCodeAuthManager().OAuthTokenIsExpired() {
            oauthToken, err = client.AuthorizationCodeAuthManager().RefreshToken(ctx)
            if err != nil {
                log.Fatalln(err)
            } else {
                // Printing the token
                fmt.Println(oauthToken)
            }
        }
        
        // Creating a new client with the token
        client = client.CloneWithConfiguration(
            spotifyWebApiWithFixesAndImprovementsFromSonallux.WithAuthorizationCodeAuthCredentials(
                client.Configuration().AuthorizationCodeAuthCredentials().
                    WithOAuthToken(oauthToken),
            ),
        )
    } else {
        // build authorization url to redirect the user
        state := "session-state"
        url := client.AuthorizationCodeAuthManager().BuildAuthorizationURL(state)
        // redirect the user to the given URL and get a code after the user consents
        authCode := GetAuthCode(url)
        
        // Fetch an access token to authorize the client
        oauthToken, err := client.AuthorizationCodeAuthManager().FetchToken(ctx, authCode)
        if err != nil {
            log.Fatalln(err)
        } else {
            // Printing the token
            fmt.Println(oauthToken)
        }
        
        // Creating a new client with the token
        client = client.CloneWithConfiguration(
            spotifyWebApiWithFixesAndImprovementsFromSonallux.WithAuthorizationCodeAuthCredentials(
                client.Configuration().AuthorizationCodeAuthCredentials().
                    WithOAuthToken(oauthToken),
            ),
        )
        
        // Store the token
        StoreInDatabase(oauthToken)
    }
    
    // The client is now authorized; you can use the client to make endpoint calls
}

func GetStoredToken() (
    models.OAuthToken,
    error) {
    // Get token logic here
    return models.OAuthToken{}, nil
}

func StoreInDatabase(oauthToken models.OAuthToken) {
    // Save token logic here
}

func GetAuthCode(redirectUrl string) string {
    // User redirection logic here
    return ""
}
```




