# Quickstart

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0aCUyRl9fZ2V0dGluZ19zdGFydGVk


# Introduction

## Introduction

The DigitalOcean API allows you to manage Droplets and resources within the
DigitalOcean cloud in a simple, programmatic way using conventional HTTP requests.

All of the functionality that you are familiar with in the DigitalOcean
control panel is also available through the API, allowing you to script the
complex actions that your situation requires.

The API documentation will start with a general overview about the design
and technology that has been implemented, followed by reference information
about specific endpoints.

### Requests

Any tool that is fluent in HTTP can communicate with the API simply by
requesting the correct URI. Requests should be made using the HTTPS protocol
so that traffic is encrypted. The interface responds to different methods
depending on the action required.

|Method|Usage|
|--- |--- |
|GET|For simple retrieval of information about your account, Droplets, or environment, you should use the GET method.  The information you request will be returned to you as a JSON object. The attributes defined by the JSON object can be used to form additional requests.  Any request using the GET method is read-only and will not affect any of the objects you are querying.|
|DELETE|To destroy a resource and remove it from your account and environment, the DELETE method should be used.  This will remove the specified object if it is found.  If it is not found, the operation will return a response indicating that the object was not found. This idempotency means that you do not have to check for a resource's availability prior to issuing a delete command, the final state will be the same regardless of its existence.|
|PUT|To update the information about a resource in your account, the PUT method is available. Like the DELETE Method, the PUT method is idempotent.  It sets the state of the target using the provided values, regardless of their current values. Requests using the PUT method do not need to check the current attributes of the object.|
|PATCH|Some resources support partial modification. In these cases, the PATCH method is available. Unlike PUT which generally requires a complete representation of a resource, a PATCH request is is a set of instructions on how to modify a resource updating only specific attributes.|
|POST|To create a new object, your request should specify the POST method. The POST request includes all of the attributes necessary to create a new object.  When you wish to create a new object, send a POST request to the target endpoint.|
|HEAD|Finally, to retrieve metadata information, you should use the HEAD method to get the headers.  This returns only the header of what would be returned with an associated GET request. Response headers contain some useful information about your API access and the results that are available for your request. For instance, the headers contain your current rate-limit value and the amount of time available until the limit resets. It also contains metrics about the total number of objects found, pagination information, and the total content length.|

### HTTP Statuses

Along with the HTTP methods that the API responds to, it will also return
standard HTTP statuses, including error codes.

In the event of a problem, the status will contain the error code, while the
body of the response will usually contain additional information about the
problem that was encountered.

In general, if the status returned is in the 200 range, it indicates that
the request was fulfilled successfully and that no error was encountered.

Return codes in the 400 range typically indicate that there was an issue
with the request that was sent. Among other things, this could mean that you
did not authenticate correctly, that you are requesting an action that you
do not have authorization for, that the object you are requesting does not
exist, or that your request is malformed.

If you receive a status in the 500 range, this generally indicates a
server-side problem. This means that we are having an issue on our end and
cannot fulfill your request currently.

400 and 500 level error responses will include a JSON object in their body,
including the following attributes:

|Name|Type|Description|
|--- |--- |--- |
|id|string|A short identifier corresponding to the HTTP status code returned. For example, the ID for a response returning a 404 status code would be "not_found."|
|message|string|A message providing additional information about the error, including details to help resolve it when possible.|
|request_id|string|Optionally, some endpoints may include a request ID that should be provided when reporting bugs or opening support tickets to help identify the issue.|

#### Example Error Response

```
HTTP/1.1 403 Forbidden
    {
      "id":       "forbidden",
      "message":  "You do not have access for the attempted action."
    }
```

### Responses

When a request is successful, a response body will typically be sent back in
the form of a JSON object. An exception to this is when a DELETE request is
processed, which will result in a successful HTTP 204 status and an empty
response body.

Inside of this JSON object, the resource root that was the target of the
request will be set as the key. This will be the singular form of the word
if the request operated on a single object, and the plural form of the word
if a collection was processed.

For example, if you send a GET request to `/v2/droplets/$DROPLET_ID` you
will get back an object with a key called "`droplet`". However, if you send
the GET request to the general collection at `/v2/droplets`, you will get
back an object with a key called "`droplets`".

The value of these keys will generally be a JSON object for a request on a
single object and an array of objects for a request on a collection of
objects.

#### Response for a Single Object

```
{
        "droplet": {
            "name": "example.com"
            . . .
        }
    }
```

#### Response for an Object Collection

```
{
        "droplets": [
            {
                "name": "example.com"
                . . .
            },
            {
                "name": "second.com"
                . . .
            }
        ]
    }
```

### Meta

In addition to the main resource root, the response may also contain a
`meta` object. This object contains information about the response itself.

The `meta` object contains a `total` key that is set to the total number of
objects returned by the request. This has implications on the `links` object
and pagination.

The `meta` object will only be displayed when it has a value. Currently, the
`meta` object will have a value when a request is made on a collection (like
`droplets` or `domains`).

#### Sample Meta Object

```
{
        . . .
        "meta": {
            "total": 43
        }
        . . .
    }
```

### Links & Pagination

The `links` object is returned as part of the response body when pagination
is enabled. By default, 20 objects are returned per page. If the response
contains 20 objects or fewer, no `links` object will be returned. If the
response contains more than 20 objects, the first 20 will be returned along
with the `links` object.

You can request a different pagination limit or force pagination by
appending `?per_page=` to the request with the number of items you would
like per page. For instance, to show only two results per page, you could
add `?per_page=2` to the end of your query. The maximum number of results
per page is 200.

The `links` object contains a `pages` object. The `pages` object, in turn,
contains keys indicating the relationship of additional pages. The values of
these are the URLs of the associated pages. The keys will be one of the
following:

* **first**: The URI of the first page of results.
* **prev**: The URI of the previous sequential page of results.
* **next**: The URI of the next sequential page of results.
* **last**: The URI of the last page of results.

The `pages` object will only include the links that make sense. So for the
first page of results, no `first` or `prev` links will ever be set. This
convention holds true in other situations where a link would not make sense.

#### Sample Links Object

```
{
        . . .
        "links": {
            "pages": {
                "last": "https://api.digitalocean.com/v2/images?page=2",
                "next": "https://api.digitalocean.com/v2/images?page=2"
            }
        }
        . . .
    }
```

### Rate Limit

Requests through the API are rate limited per OAuth token. Current rate limits:

* 5,000 requests per hour
* 250 requests per minute (5% of the hourly total)

Once you exceed either limit, you will be rate limited until the next cycle
starts. Space out any requests that you would otherwise issue in bursts for
the best results.

The rate limiting information is contained within the response headers of
each request. The relevant headers are:

* **ratelimit-limit**: The number of requests that can be made per hour.
* **ratelimit-remaining**: The number of requests that remain before you hit your request limit. See the information below for how the request limits expire.
* **ratelimit-reset**: This represents the time when the oldest request will expire. The value is given in [Unix epoch time](http://en.wikipedia.org/wiki/Unix_time). See below for more information about how request limits expire.

As long as the `ratelimit-remaining` count is above zero, you will be able
to make additional requests.

The way that a request expires and is removed from the current limit count
is important to understand. Rather than counting all of the requests for an
hour and resetting the `ratelimit-remaining` value at the end of the hour,
each request instead has its own timer.

This means that each request contributes toward the `ratelimit-remaining`
count for one complete hour after the request is made. When that request's
timer runs out, it is no longer counted towards the request limit.

This has implications on the meaning of the `ratelimit-reset` header as
well. Because the entire rate limit is not reset at one time, the value of
this header is set to the time when the _oldest_ request will expire.

Keep this in mind if you see your `ratelimit-reset` value change, but not
move an entire hour into the future.

If the `ratelimit-remaining` reaches zero, subsequent requests will receive
a 429 error code until the request reset has been reached. You can see the
format of the response in the examples.

**Note:** The following endpoints have special rate limit requirements that
are independent of the limits defined above.

* Only 12 `POST` requests to the `/v2/floating_ips` endpoint to create Floating IPs can be made per 60 seconds.
* Only 10 `GET` requests to the `/v2/account/keys` endpoint to list SSH keys can be made per 60 seconds.
* Only 5 requests to any and all `v2/cdn/endpoints` can be made per 10 seconds. This includes `v2/cdn/endpoints`,
  `v2/cdn/endpoints/$ENDPOINT_ID`, and `v2/cdn/endpoints/$ENDPOINT_ID/cache`.
* Only 50 strings within the `files` json struct in the `v2/cdn/endpoints/$ENDPOINT_ID/cache` [payload](https://docs.digitalocean.com/reference/api/api-reference/#operation/cdn_purge_cache)
  can be requested every 20 seconds.

#### Sample Rate Limit Headers

```
. . .
    ratelimit-limit: 1200
    ratelimit-remaining: 1193
    rateLimit-reset: 1402425459
    . . .
```

#### Sample Rate Exceeded Response

```
429 Too Many Requests
    {
            id: "too_many_requests",
            message: "API Rate limit exceeded."
    }
```

### Curl Examples

Throughout this document, some example API requests will be given using the
`curl` command. This will allow us to demonstrate the various endpoints in a
simple, textual format.

These examples assume that you are using a Linux or macOS command line. To run
these commands on a Windows machine, you can either use cmd.exe, PowerShell, or WSL:

* For cmd.exe, use the `set VAR=VALUE` [syntax](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/set_1)
  to define environment variables, call them with `%VAR%`, then replace all backslashes (`\`) in the examples with carets (`^`).

* For PowerShell, use the `$Env:VAR = "VALUE"` [syntax](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_environment_variables?view=powershell-7.2)
  to define environment variables, call them with `$Env:VAR`, then replace `curl` with `curl.exe` and all backslashes (`\`) in the examples with backticks (`` ` ``).

* WSL is a compatibility layer that allows you to emulate a Linux terminal on a Windows machine.
  Install WSL with our [community tutorial](https://www.digitalocean.com/community/tutorials/how-to-install-the-windows-subsystem-for-linux-2-on-microsoft-windows-10),
  then follow this API documentation normally.

The names of account-specific references (like Droplet IDs, for instance)
will be represented by variables. For instance, a Droplet ID may be
represented by a variable called `$DROPLET_ID`. You can set the associated
variables in your environment if you wish to use the examples without
modification.

The first variable that you should set to get started is your OAuth
authorization token. The next section will go over the details of this, but
you can set an environmental variable for it now.

Generate a token by going to the [Apps & API](https://cloud.digitalocean.com/settings/applications)
section of the DigitalOcean control panel. Use an existing token if you have
saved one, or generate a new token with the "Generate new token" button.
Copy the generated token and use it to set and export the TOKEN variable in
your environment as the example shows.

You may also wish to set some other variables now or as you go along. For
example, you may wish to set the `DROPLET_ID` variable to one of your
Droplet IDs since this will be used frequently in the API.

If you are following along, make sure you use a Droplet ID that you control
so that your commands will execute correctly.

If you need access to the headers of a response through `curl`, you can pass
the `-i` flag to display the header information along with the body. If you
are only interested in the header, you can instead pass the `-I` flag, which
will exclude the response body entirely.

#### Set and Export your OAuth Token

```
export DIGITALOCEAN_TOKEN=your_token_here
```

#### Set and Export a Variable

```
export DROPLET_ID=1111111
```

### Parameters

There are two different ways to pass parameters in a request with the API.

When passing parameters to create or update an object, parameters should be
passed as a JSON object containing the appropriate attribute names and
values as key-value pairs. When you use this format, you should specify that
you are sending a JSON object in the header. This is done by setting the
`Content-Type` header to `application/json`. This ensures that your request
is interpreted correctly.

When passing parameters to filter a response on GET requests, parameters can
be passed using standard query attributes. In this case, the parameters
would be embedded into the URI itself by appending a `?` to the end of the
URI and then setting each attribute with an equal sign. Attributes can be
separated with a `&`. Tools like `curl` can create the appropriate URI when
given parameters and values; this can also be done using the `-F` flag and
then passing the key and value as an argument. The argument should take the
form of a quoted string with the attribute being set to a value with an
equal sign.

#### Pass Parameters as a JSON Object

```
curl -H "Authorization: Bearer $DIGITALOCEAN_TOKEN" \
        -H "Content-Type: application/json" \
        -d '{"name": "example.com", "ip_address": "127.0.0.1"}' \
        -X POST "https://api.digitalocean.com/v2/domains"
```

#### Pass Filter Parameters as a Query String

```
curl -H "Authorization: Bearer $DIGITALOCEAN_TOKEN" \
         -X GET \
         "https://api.digitalocean.com/v2/images?private=true"
```

### Cross Origin Resource Sharing

In order to make requests to the API from other domains, the API implements
Cross Origin Resource Sharing (CORS) support.

CORS support is generally used to create AJAX requests outside of the domain
that the request originated from. This is necessary to implement projects
like control panels utilizing the API. This tells the browser that it can
send requests to an outside domain.

The procedure that the browser initiates in order to perform these actions
(other than GET requests) begins by sending a "preflight" request. This sets
the `Origin` header and uses the `OPTIONS` method. The server will reply
back with the methods it allows and some of the limits it imposes. The
client then sends the actual request if it falls within the allowed
constraints.

This process is usually done in the background by the browser, but you can
use curl to emulate this process using the example provided. The headers
that will be set to show the constraints are:

* **Access-Control-Allow-Origin**: This is the domain that is sent by the client or browser as the origin of the request. It is set through an `Origin` header.
* **Access-Control-Allow-Methods**: This specifies the allowed options for requests from that domain. This will generally be all available methods.
* **Access-Control-Expose-Headers**: This will contain the headers that will be available to requests from the origin domain.
* **Access-Control-Max-Age**: This is the length of time that the access is considered valid. After this expires, a new preflight should be sent.
* **Access-Control-Allow-Credentials**: This will be set to `true`. It basically allows you to send your OAuth token for authentication.

You should not need to be concerned with the details of these headers,
because the browser will typically do all of the work for you.


# Building

The generated code depends on a few Ruby gems. The references to these gems are added in the gemspec file. The easiest way to resolve the dependencies, build the gem and install it is through Rake:

1. Install Rake if not already installed: `gem install rake`
2. Install Bundler if not already installed: `gem install bundler`
3. From terminal/cmd navigate to the root directory of the SDK.
4. Invoke: `rake install`

Alternatively, you can build and install the gem manually:

1. From terminal/cmd navigate to the root directory of the SDK.
2. Run the build command: `gem build digital_ocean_api.gemspec`
3. Run the install command: `gem install digital_ocean_api-2.0.0.gem`

![Installing Gem](https://apidocs.io/illustration/ruby?workspaceFolder=DigitalOceanApi&gemVer=2.0.0&gemName=digital_ocean_api&step=buildSDK)


# Installation

The following section explains how to use the digital_ocean_api ruby gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

## 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting `File -> Close Project`. Next, click on `Create New Project` to create a new project from scratch.

![Create a new project in RubyMine - Step 1](https://apidocs.io/illustration/ruby?workspaceFolder=DigitalOceanApi&step=createNewProject0)

Next, provide `TestApp` as the project name, choose `Rails Application` as the project type, and click `OK`.

![Create a new Rails Application in RubyMine - Step 2](https://apidocs.io/illustration/ruby?workspaceFolder=DigitalOceanApi&step=createNewProject1)

In the next dialog make sure that the correct Ruby SDK is being used (>= 2.6 and <= 3.2) and click `OK`.

![Create a new Rails Application in RubyMine - Step 3](https://apidocs.io/illustration/ruby?workspaceFolder=DigitalOceanApi&step=createNewProject2)

## 2. Add reference of the gem

In order to use the `digital_ocean_api` gem in the new project we must add a gem reference. Locate the `Gemfile` in the Project Explorer window under the `TestApp` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: `gem 'digital_ocean_api', '2.0.0'`

![Add new reference to the Gemfile](https://apidocs.io/illustration/ruby?workspaceFolder=DigitalOceanApi&gemVer=2.0.0&gemName=digital_ocean_api&step=addReference)

## 3. Adding a new Rails Controller

Once the `TestApp` project is created, a folder named `controllers` will be visible in the *Project Explorer* under the following path: `TestApp > app > controllers`. Right click on this folder and select `New -> Run Rails Generator...`.

![Run Rails Generator on Controllers Folder](https://apidocs.io/illustration/ruby?workspaceFolder=DigitalOceanApi&gemVer=2.0.0&gemName=digital_ocean_api&step=addCode0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the `controller` template.

![Create a new Controller](https://apidocs.io/illustration/ruby?workspaceFolder=DigitalOceanApi&step=addCode1)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide `Hello` and include an action named `Index` and click `OK`.

![Add a new Controller](https://apidocs.io/illustration/ruby?workspaceFolder=DigitalOceanApi&gemVer=2.0.0&gemName=digital_ocean_api&step=addCode2)

A new controller class named `HelloController` will be created in a file named `hello_controller.rb` containing a method named `Index`.

1. Add the `require 'digital_ocean_api'` statement to require the gem in the controller file.
2. Add the `include DigitalOceanApi` statement to include the sdk module in the controller file.
3. In the `Index` method, add code for initialization and a sample for its usage.

![Initialize the library](https://apidocs.io/illustration/ruby?workspaceFolder=DigitalOceanApi&gemName=digital_ocean_api&step=addCode3)



# Initialize the API Client

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| connection | `Faraday::Connection` | The Faraday connection object passed by the SDK user for making requests |
| adapter | `Faraday::Adapter` | The Faraday adapter object passed by the SDK user for performing http requests |
| timeout | `Float` | The value to use for connection timeout. <br> **Default: 30** |
| max_retries | `Integer` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| retry_interval | `Float` | Pause in seconds between retries. <br> **Default: 1** |
| backoff_factor | `Float` | The amount to multiply each successive retry's interval amount by in order to provide backoff. <br> **Default: 2** |
| retry_statuses | `Array` | A list of HTTP statuses to retry. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array` | A list of HTTP methods to retry. <br> **Default: %i[get put get put]** |
| http_callback | `HttpCallBack` | The Http CallBack allows defining callables for pre and post API calls. |
| proxy_settings | [`ProxySettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/configuration/proxysettings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/configuration/loggingconfiguration.md) | The SDK logging configuration for API calls |
| bearer_auth_credentials | [`BearerAuthCredentials`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md) | The credential object for OAuth 2 Bearer token |

The API client can be initialized as follows:

## Code-Based Client Initialization

```ruby
require 'digital_ocean_api'
include DigitalOceanApi

client = Client.new(
  bearer_auth_credentials: BearerAuthCredentials.new(
    access_token: 'AccessToken'
  ),
  logging_configuration: LoggingConfiguration.new(
    log_level: Logger::INFO,
    request_logging_config: RequestLoggingConfiguration.new(
      log_body: true
    ),
    response_logging_config: ResponseLoggingConfiguration.new(
      log_headers: true
    )
  )
)
```

## Environment-Based Client Initialization

```ruby
require 'digital_ocean_api'
include DigitalOceanApi

# Create client from environment
client = Client.from_env
```

See the [`Environment-Based Client Initialization`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/sdk-infrastructure/configuration/environment-based-client-initialization.md) section for details.


# Authorization

This API uses the following authentication schemes.

* [`bearer_auth (OAuth 2 Bearer token)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)

## bearer_auth (OAuth 2 Bearer token)



Documentation for accessing and setting credentials for bearer_auth.

### Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| AccessToken | `String` | The OAuth 2.0 Access Token to use for API requests. | `access_token` |



**Note:** Auth credentials can be set using named parameter for any of the above credentials (e.g. `access_token`) in the client initialization.

### Usage Example

#### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```ruby
require 'digital_ocean_api'
include DigitalOceanApi

client = Client.new(
  bearer_auth_credentials: BearerAuthCredentials.new(
    access_token: 'AccessToken'
  )
)
```




