---
layout: "newrelic"
page_title: "New Relic: newrelic_plugin"
sidebar_current: "docs-newrelic-datasource-plugin"
description: |-
  Looks up the information about a plugin in New Relic.
---

# Data Source: newrelic\_plugin

~> **DEPRECATED** This data source is deprecated and will stop being supported as of June 16, 2021. For more information, check out [https://discuss.newrelic.com/t/new-relic-plugin-eol-wednesday-june-16th-2021/127267](https://discuss.newrelic.com/t/new-relic-plugin-eol-wednesday-june-16th-2021/127267)

Use this data source to get information about a specific installed plugin in New Relic. More information on Terraform's data sources can be found [here](https://www.terraform.io/docs/configuration/data-sources.html).

Each plugin published to New Relic's Plugin Central is assigned a [GUID](https://docs.newrelic.com/docs/plugins/plugin-developer-resources/planning-your-plugin/parts-plugin#guid). Once you have installed a plugin into your account it is assigned an ID. This account-specific ID is required when creating Plugins alert conditions.

## Example Usage

```hcl
data "newrelic_plugin" "foo" {
  guid = "com.example.my-plugin"
}

```

## Argument Reference

The following arguments are supported:

* `guid` - (Required) The GUID of the plugin in New Relic.

## Attributes Reference

In addition to all arguments above, the following attributes are exported:

* `id` - The ID of the installed plugin instance.
