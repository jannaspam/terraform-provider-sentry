---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "sentry_key Data Source - terraform-provider-sentry"
subcategory: ""
description: |-
  Sentry Key data source.
---

# sentry_key (Data Source)

Sentry Key data source.

## Example Usage

```terraform
# Retrieve the Default Key
data "sentry_key" "default" {
  organization = "my-organization"

  project = "web-app"
  name    = "Default"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `organization` (String) The slug of the organization the key should be created for.
- `project` (String) The slug of the project the key should be created for.

### Optional

- `first` (Boolean) Boolean flag indicating that we want the first key of the returned keys.
- `name` (String) The name of the key to retrieve.

### Read-Only

- `dsn_csp` (String) DSN for the Content Security Policy (CSP) for the key.
- `dsn_public` (String) DSN for the key.
- `dsn_secret` (String, Deprecated)
- `id` (String) The ID of this resource.
- `is_active` (Boolean) Flag indicating the key is active.
- `project_id` (Number) The ID of the project that the key belongs to.
- `public` (String) Public key portion of the client key.
- `rate_limit_count` (Number) Number of events that can be reported within the rate limit window.
- `rate_limit_window` (Number) Length of time that will be considered when checking the rate limit.
- `secret` (String) Secret key portion of the client key.


