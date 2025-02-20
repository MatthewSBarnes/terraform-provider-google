---
# ----------------------------------------------------------------------------
#
#     ***     AUTO GENERATED CODE    ***    Type: MMv1     ***
#
# ----------------------------------------------------------------------------
#
#     This file is automatically generated by Magic Modules and manual
#     changes will be clobbered when the file is regenerated.
#
#     Please read more about how to change this file in
#     .github/CONTRIBUTING.md.
#
# ----------------------------------------------------------------------------
subcategory: "API Gateway"
layout: "google"
page_title: "Google: google_api_gateway_api"
sidebar_current: "docs-google-api-gateway-api"
description: |-
  A consumable API that can be used by multiple Gateways.
---

# google\_api\_gateway\_api

A consumable API that can be used by multiple Gateways.

~> **Warning:** This resource is in beta, and should be used with the terraform-provider-google-beta provider.
See [Provider Versions](https://terraform.io/docs/providers/google/guides/provider_versions.html) for more details on beta resources.

To get more information about Api, see:

* [API documentation](https://cloud.google.com/api-gateway/docs/reference/rest/v1beta/projects.locations.apis)
* How-to Guides
    * [Official Documentation](https://cloud.google.com/api-gateway/docs/quickstart)

<div class = "oics-button" style="float: right; margin: 0 0 -15px">
  <a href="https://console.cloud.google.com/cloudshell/open?cloudshell_git_repo=https%3A%2F%2Fgithub.com%2Fterraform-google-modules%2Fdocs-examples.git&cloudshell_working_dir=apigateway_api_basic&cloudshell_image=gcr.io%2Fgraphite-cloud-shell-images%2Fterraform%3Alatest&open_in_editor=main.tf&cloudshell_print=.%2Fmotd&cloudshell_tutorial=.%2Ftutorial.md" target="_blank">
    <img alt="Open in Cloud Shell" src="//gstatic.com/cloudssh/images/open-btn.svg" style="max-height: 44px; margin: 32px auto; max-width: 100%;">
  </a>
</div>
## Example Usage - Apigateway Api Basic


```hcl
resource "google_api_gateway_api" "api" {
  provider = google-beta
  api_id = "api"
}
```

## Argument Reference

The following arguments are supported:


* `api_id` -
  (Required)
  Identifier to assign to the API. Must be unique within scope of the parent resource(project)


- - -


* `display_name` -
  (Optional)
  A user-visible name for the API.

* `managed_service` -
  (Optional)
  Immutable. The name of a Google Managed Service ( https://cloud.google.com/service-infrastructure/docs/glossary#managed).
  If not specified, a new Service will automatically be created in the same project as this API.

* `labels` -
  (Optional)
  Resource labels to represent user-provided metadata.

* `project` - (Optional) The ID of the project in which the resource belongs.
    If it is not provided, the provider project is used.


## Attributes Reference

In addition to the arguments listed above, the following computed attributes are exported:

* `id` - an identifier for the resource with format `projects/{{project}}/locations/global/apis/{{api_id}}`

* `name` -
  The resource name of the API. Format `projects/{{project}}/locations/global/apis/{{apiId}}`

* `create_time` -
  Creation timestamp in RFC3339 text format.


## Timeouts

This resource provides the following
[Timeouts](/docs/configuration/resources.html#timeouts) configuration options:

- `create` - Default is 6 minutes.
- `update` - Default is 6 minutes.
- `delete` - Default is 6 minutes.

## Import


Api can be imported using any of these accepted formats:

```
$ terraform import google_api_gateway_api.default projects/{{project}}/locations/global/apis/{{api_id}}
$ terraform import google_api_gateway_api.default {{project}}/{{api_id}}
$ terraform import google_api_gateway_api.default {{api_id}}
```

## User Project Overrides

This resource supports [User Project Overrides](https://www.terraform.io/docs/providers/google/guides/provider_reference.html#user_project_override).
