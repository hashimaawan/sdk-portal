# Getting Started

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/java/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

Furkot provides Rest API to access user trip data.
Using Furkot API an application can list user trips and display stops for a specific trip.
Furkot API uses OAuth2 protocol to authorize applications to access data on behalf of users.

Furkot API description: [https://help.furkot.com/widgets/furkot-api.html](https://help.furkot.com/widgets/furkot-api.html)


# Building

Supported Java version is **8+**.

The generated code uses a few Maven dependencies e.g., Jackson, OkHttp,
and Apache HttpClient. The reference to these dependencies is already
added in the pom.xml file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Eclipse click on `File -> Import`.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=import0)

* In the import dialog, select `Existing Java Project` and click `Next`.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=import1)

* Browse to locate the folder containing the source code. Select the detected location of the project and click `Finish`.

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=import2)

* Upon successful import, the project will be automatically built by Eclipse after automatically resolving the dependencies.

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=import3)

* After successfully building the project, the client library needs to be installed as a Maven package in your local cache. Right-click on the project, select `Show in Local Terminal -> Terminal` or use `Ctrl + Alt + T` to open Terminal.

![Importing SDK into Eclipse - Step 5](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=openTerminal)

* In the terminal dialog, run the following command to install client library.

```
mvn install -Dmaven.test.skip=true -Dmaven.javadoc.skip=true
```

![Importing SDK into Eclipse - Step 6](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=installCommand)


# Installation

The following section explains how to use the FurkotTripsLib library in a new project.

## 1. Starting a new project

For starting a new project, click the menu command `File > New > Project`.

![Add a new project in Eclipse](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=createNewProject0)

Next, choose `Maven > Maven Project` and click `Next`.

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=createNewProject1)

Here, make sure to use the current workspace by choosing `Use default Workspace location`, as shown in the picture below and click `Next`.

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=createNewProject2)

Following this, select the *quick start* project type to create a simple project with an existing class and a `main` method. To do this, choose `maven-archetype-quickstart` item from the list and click `Next`.

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=createNewProject3)

In the last step, provide a `Group Id` and `Artifact Id` as shown in the picture below and click `Finish`.

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=createNewProject4)

## 2. Add reference of the library project

The created Maven project manages its dependencies using its `pom.xml` file. In order to add a dependency on the *FurkotTripsLib* client library, double click on the `pom.xml` file in the `Package Explorer`. Opening the `pom.xml` file will render a graphical view on the canvas. Here, switch to the `Dependencies` tab and click the `Add` button as shown in the picture below.

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=testProject0)

Clicking the `Add` button will open a dialog where you need to specify FurkotTripsLib in `Group Id`, furkot-trips-lib in `Artifact Id` and 1.0.0 in the `Version` fields. Once added click `OK`. Save the `pom.xml` file.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=testProject1)

![Adding sample code](https://apidocs.io/illustration/java?workspaceFolder=Furkot%20Trips-Java&workspaceName=FurkotTrips&projectName=FurkotTripsLib&rootNamespace=com.furkot.trips&groupId=FurkotTripsLib&artifactId=furkot-trips-lib&version=1.0.0&step=testProject2)

## 3. Write sample code

Once the `SimpleConsoleApp` is created, a file named `App.java` will be visible in the *Package Explorer* with a `main` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.


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
| environment | [`Environment`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/java/getting-started/environments.md) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpClientConfig | [`Consumer<HttpClientConfiguration.Builder>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/java/sdk-infrastructure/configuration/httpclientconfiguration-builder.md) | Set up Http Client Configuration instance. |
| furkotAuthAccessCodeCredentials | [`FurkotAuthAccessCodeCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/java/getting-started/authorization.md) | The Credentials Setter for OAuth 2 Authorization Code Grant |
| furkotAuthImplicitCredentials | [`FurkotAuthImplicitCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/java/getting-started/authorization.md) | The Credentials Setter for OAuth 2 Implicit Grant |

The API client can be initialized as follows:

```java
import com.furkot.trips.Environment;
import com.furkot.trips.FurkotTripsClient;
import com.furkot.trips.authentication.FurkotAuthAccessCodeModel;
import com.furkot.trips.authentication.FurkotAuthImplicitModel;
import com.furkot.trips.exceptions.ApiException;
import com.furkot.trips.models.OAuthScopeFurkotAuthAccessCodeEnum;
import com.furkot.trips.models.OAuthScopeFurkotAuthImplicitEnum;
import com.furkot.trips.models.OAuthToken;
import java.io.IOException;
import java.util.Arrays;

public class Program {
    public static void main(String[] args) {
        FurkotTripsClient client = new FurkotTripsClient.Builder()
            .httpClientConfig(configBuilder -> configBuilder
                    .timeout(0))
            .furkotAuthAccessCodeCredentials(new FurkotAuthAccessCodeModel.Builder(
                    "OAuthClientId",
                    "OAuthClientSecret",
                    "OAuthRedirectUri"
                )
                .oAuthScopes(Arrays.asList(
                        OAuthScopeFurkotAuthAccessCodeEnum.READTRIPS
                    ))
                .build())
            .furkotAuthImplicitCredentials(new FurkotAuthImplicitModel.Builder(
                    "OAuthClientId",
                    "OAuthRedirectUri"
                )
                .oAuthScopes(Arrays.asList(
                        OAuthScopeFurkotAuthImplicitEnum.READTRIPS
                    ))
                .build())
            .environment(Environment.PRODUCTION)
            .build();

    }
}
```


# Authorization

This API uses the following authentication schemes.

* [`furkot_auth_access_code (OAuth 2 Authorization Code Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/java/getting-started/authorization.md)
* [`furkot_auth_implicit (OAuth 2 Implicit Grant)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/java/getting-started/authorization.md)

## furkot_auth_access_code (OAuth 2 Authorization Code Grant)



Documentation for accessing and setting credentials for furkot_auth_access_code.

### Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| OAuthClientId | `String` | OAuth 2 Client ID | `oAuthClientId` | `getOAuthClientId()` |
| OAuthClientSecret | `String` | OAuth 2 Client Secret | `oAuthClientSecret` | `getOAuthClientSecret()` |
| OAuthRedirectUri | `String` | OAuth 2 Redirection endpoint or Callback Uri | `oAuthRedirectUri` | `getOAuthRedirectUri()` |
| OAuthToken | `OAuthToken` | Object for storing information about the OAuth token | `oAuthToken` | `getOAuthToken()` |
| OAuthScopes | `List<OAuthScopeFurkotAuthAccessCodeEnum>` | List of scopes that apply to the OAuth token | `oAuthScopes` | `getOAuthScopes()` |



**Note:** Auth credentials can be set using `furkotAuthAccessCodeCredentials` in the client builder and accessed through `getFurkotAuthAccessCodeCredentials` method in the client instance.

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```java
import com.furkot.trips.FurkotTripsClient;
import com.furkot.trips.authentication.FurkotAuthAccessCodeModel;
import com.furkot.trips.exceptions.ApiException;
import com.furkot.trips.models.OAuthScopeFurkotAuthAccessCodeEnum;
import com.furkot.trips.models.OAuthToken;
import java.io.IOException;
import java.util.Arrays;

public class Program {
    public static void main(String[] args) {
        FurkotTripsClient client = new FurkotTripsClient.Builder()
            .furkotAuthAccessCodeCredentials(new FurkotAuthAccessCodeModel.Builder(
                    "OAuthClientId",
                    "OAuthClientSecret",
                    "OAuthRedirectUri"
                )
                .oAuthScopes(Arrays.asList(
                        OAuthScopeFurkotAuthAccessCodeEnum.READTRIPS
                    ))
                .build())
            .build();
    }
}
```



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Authorization Code Grant*. This authorization includes the following steps

### 2\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page.The `buildAuthorizationUrl()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```java
String authUrl = client.getFurkotAuthAccessCode().buildAuthorizationUrl(); // build auth url
httpServletResponse.sendRedirect(authUrl); // show user the auth page in a browser or by redirection
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

```java
try {
    String authorizationCode = "Replace me with actual authorization code";
    OAuthToken token = client.getFurkotAuthAccessCodeCredentials().fetchToken(authorizationCode);
    // re-instantiate the client with oauth token
    client = client.newBuilder()
            .furkotAuthAccessCodeCredentials(client.getFurkotAuthAccessCodeModel().toBuilder()
                    .oAuthToken(token)
                    .build())
            .build();
} catch (Throwable e) {
    // TODO Handle exception
}
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeFurkotAuthAccessCodeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/java/models/enumerations/o-auth-scope-furkot-auth-access-code.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list trips and stops info |

### Refreshing the token

An access token may expire after sometime. To extend its lifetime, you must refresh the token.

```java
if (client.getFurkotAuthAccessCodeCredentials().isTokenExpired()) {
    try {
        OAuthToken token = client.getFurkotAuthAccessCodeCredentials().refreshToken();
        // re-instantiate the client with oauth token
        client = client.newBuilder()
                .furkotAuthAccessCodeCredentials(client.getFurkotAuthAccessCodeModel().toBuilder()
                        .oAuthToken(token)
                        .build())
                .build();
    } catch (Throwable e) {
        // TODO Handle exception
    }
}
```

If a token expires, an exception will be thrown before the next endpoint call requiring authentication.

### Storing an access token for reuse

It is recommended that you store the access token for reuse.

```java
// store token
httpSession.setAttribute("access_token", client.getFurkotAuthAccessCodeCredentials().getOAuthToken());
```

### Creating a client from a stored token

To authorize a client using a stored access token, just set the access token in Configuration along with the other configuration parameters before creating the client:

```java
// load token later...
OAuthToken token = (OAuthToken) httpSession.getAttribute("access_token");

// re-instantiate the client with oauth token
client = client.newBuilder()
        .furkotAuthAccessCodeCredentials(client.getFurkotAuthAccessCodeModel().toBuilder()
                .oAuthToken(token)
                .build())
        .build();
```

### Complete example



In this example that uses the Spring framework and an application using spring framework can be easily set up through [`spring initializr`](https://start.spring.io/), the `/callapi` route will first check if an access token is available for the user. If one is not set,
it redirects the user to `/authcallback` route which will obtain an access token and redirect the user back to the `/callapi` route.
Now that an access token is set, `/callapi` route can use the client to make authorized calls to the server.

#### `MainController.java`

```java
package com.example;

import com.furkot.trips.FurkotTripsClient;
import com.furkot.trips.authentication.FurkotAuthAccessCodeModel;
import com.furkot.trips.models.OAuthScopeEnum;
import com.furkot.trips.models.OAuthToken;
import jakarta.servlet.http.HttpServletResponse;
import jakarta.servlet.http.HttpSession;
import java.util.Arrays;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestMethod;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;

@RestController
@RequestMapping("/")
public class MainController {
    private FurkotTripsClient client;

    public MainController() {
        client = new FurkotTripsClient.Builder()
            .furkotAuthAccessCodeCredentials(new FurkotAuthAccessCodeModel.Builder(
                    "OAuthClientId",
                    "OAuthClientSecret",
                    "OAuthRedirectUri"
                )
                .oAuthScopes(Arrays.asList(
                        OAuthScopeFurkotAuthAccessCodeEnum.READTRIPS
                    ))
                .build())
            .build();
    }

    @RequestMapping(value = "/callapi", method = RequestMethod.GET, produces = "application/json")
    public String callApi(HttpSession session, HttpServletResponse response) throws Throwable {
        // redirect if access token is not set
        if (session.getAttribute("access_token") == null) {
            response.sendRedirect("authcallback");
            return null;
        }

        synchronized (client) {
            client = client.newBuilder()
                    .furkotAuthAccessCodeCredentials(client.getFurkotAuthAccessCodeModel().toBuilder()
                            .oAuthToken((OAuthToken) session.getAttribute("access_token"))
                            .build())
                    .build();

            // refresh the token if it is expired
            if(client.getFurkotAuthAccessCodeCredentials().isTokenExpired()) {
                try {
                    OAuthToken token = client.getFurkotAuthAccessCodeCredentials().refreshToken();
                    session.setAttribute("access_token", token);
                    // re-instantiate the client with oauth token
                    client = client.newBuilder()
                            .furkotAuthAccessCodeCredentials(client.getFurkotAuthAccessCodeModel().toBuilder()
                                    .oAuthToken(token)
                                    .build())
                            .build();
                } catch (Throwable e) {
                    // TODO Handle exception
                }
            }

            // now you can use client to make endpoint calls
            // client will automatically refresh the token when it expires
            return "someView";
        }
    }

    @RequestMapping(value = "/authcallback", method = RequestMethod.GET)
    public void authcallback(HttpSession session, @RequestParam(required = false) String code,
            HttpServletResponse response) throws Throwable {
        if (code == null) {
            String authUrl;
            
            synchronized (client) {
                authUrl = client.getFurkotAuthAccessCodeCredentials().buildAuthorizationUrl();
            }
            
            // if authorization code is absent, redirect to authorization page
            response.sendRedirect(authUrl);
        } else {
            OAuthToken token;
            
            synchronized (client) {
                token = client.getFurkotAuthAccessCodeCredentials().fetchToken(code);
                // re-instantiate the client with oauth token
                client = client.newBuilder()
                        .furkotAuthAccessCodeCredentials(client.getFurkotAuthAccessCodeModel().toBuilder()
                                .oAuthToken(token)
                                .build())
                        .build();
            }
            
            session.setAttribute("access_token", token);
            response.sendRedirect("callapi");
        }
    }
}
```

## furkot_auth_implicit (OAuth 2 Implicit Grant)



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Implicit Grant* to obtain a user's consent to perform an API request on user's behalf. This authorization includes the following steps

This process requires the presence of a client-side JavaScript code on the redirect URI page to receive the *access token* after the consent step is completed.

### 1\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page. The `buildAuthorizationUrl()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```java
String authUrl = client.getFurkotAuthImplicit().buildAuthorizationUrl(); // build auth url
httpServletResponse.sendRedirect(authUrl); // show user the auth page in a browser or by redirection
```

### 2\. Handle the OAuth server response

Once the user responds to the consent request, the OAuth 2.0 server responds to your application's access request by redirecting the user to the redirect URI specified set in `Configuration`.

The redirect URI will receive the *access token* as the `token` argument in the URL fragment.

```
https://example.com/oauth/callback#token=XXXXXXXXXXXXXXXXXXXXXXXXX
```

The access token must be extracted by the client-side JavaScript code. The access token can be used to authorize any further endpoint calls by the JavaScript code.

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeFurkotAuthImplicitEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/java/models/enumerations/o-auth-scope-furkot-auth-implicit.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `READTRIPS` | list users trips info |




