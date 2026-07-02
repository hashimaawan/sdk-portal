# Default Toast Compression

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkRlZmF1bHRUb2FzdENvbXByZXNzaW9u

Specifies the default TOAST compression method for values of compressible columns (the default is lz4).


# Enum Type Name

`DefaultToastCompression`


# Fields

| Name |
|  --- |
| `LZ4` |
| `PGLZ` |


# Example

```ruby
default_toast_compression = DefaultToastCompression::LZ4
```



