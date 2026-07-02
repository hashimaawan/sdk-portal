# Links Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpbmtzUGFnZXM


# Class Name

`LinksPages`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`Pages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/pages.md) | LinksPages.FromPages(Pages pages) |
| [`Pages1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/pages-1.md) | LinksPages.FromPages1(Pages1 pages1) |
| [`object`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | LinksPages.FromObject(object mObject) |


# Pages

## Initialization Code

### Example

```csharp
LinksPages value = LinksPages.FromPages(
    new Pages
    {
        Last = "https://api.digitalocean.com/v2/images?page=2",
        Next = "https://api.digitalocean.com/v2/images?page=2",
    }
);
```


# Pages1

## Initialization Code

### Example

```csharp
LinksPages value = LinksPages.FromPages1(
    new Pages1
    {
        First = "https://api.digitalocean.com/v2/images?page=1",
        Prev = "https://api.digitalocean.com/v2/images?page=1",
    }
);
```


# object

## Initialization Code

### Example

```csharp
LinksPages value = LinksPages.FromObject(
    ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}")
);
```



