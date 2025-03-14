---
page_title: "Sentry Provider"
description: |-
  Terraform provider for Sentry.
---

# Sentry Provider

Terraform provider for [Sentry](https://sentry.io).

## Example Usage

```terraform
# Configure the Sentry Provider
provider "sentry" {
  token = var.sentry_auth_token

  # If you are self-hosting Sentry, set the base URL here.
  # The URL format must be "https://[hostname]/api/".
  # base_url = "https://example.com/api/"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `token` (String, Sensitive) The authentication token used to connect to Sentry. The value can be sourced from the `SENTRY_AUTH_TOKEN` environment variable.

### Optional

- `base_url` (String) The target Sentry Base API URL in the format `https://[hostname]/api/`. The default value is `https://sentry.io/api/`. The value must be provided when working with Sentry On-Premise. The value can be sourced from the `SENTRY_BASE_URL` environment variable.


