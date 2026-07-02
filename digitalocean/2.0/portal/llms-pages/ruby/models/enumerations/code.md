# Code

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvZGU

A code identifier that represents the failing condition.

Failing conditions:

- `incompatible_phase` - indicates that the deployment's phase is not suitable for rollback.
- `incompatible_result` - indicates that the deployment's result is not suitable for rollback.
- `exceeded_revision_limit` - indicates that the app has exceeded the rollback revision limits for its tier.
- `app_pinned` - indicates that there is already a rollback in progress and the app is pinned.
- `database_config_conflict` - indicates that the deployment's database config is different than the current config.
- `region_conflict` - indicates that the deployment's region differs from the current app region.

Warning conditions:

- `static_site_requires_rebuild` - indicates that the deployment contains at least one static site that will require a rebuild.
- `image_source_missing_digest` - indicates that the deployment contains at least one component with an image source that is missing a digest.


# Enum Type Name

`Code`


# Fields

| Name |
|  --- |
| `INCOMPATIBLE_PHASE` |
| `INCOMPATIBLE_RESULT` |
| `EXCEEDED_REVISION_LIMIT` |
| `APP_PINNED` |
| `DATABASE_CONFIG_CONFLICT` |
| `REGION_CONFLICT` |
| `STATIC_SITE_REQUIRES_REBUILD` |
| `IMAGE_SOURCE_MISSING_DIGEST` |


# Example

```ruby
code = Code::EXCEEDED_REVISION_LIMIT
```



