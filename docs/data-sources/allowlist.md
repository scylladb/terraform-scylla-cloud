---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "scyllacloud_allowlist Data Source - terraform-provider-scyllacloud"
subcategory: ""
description: |-
  Cluster firewall rules data source
---

# scyllacloud_allowlist (Data Source)

Cluster firewall rules data source

## Example Usage

```terraform
data "scyllacloud_cluster" "example" {
  name = "example"
}

data "scyllacloud_allowslist" "example" {
  cluster_id = data.scyllacloud_cluster.example.id
}

output "cluster_allowed_ips" {
  value = data.scyllacloud_allowslist.example.all[*].source_address
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `cluster_id` (Number) ID of the cluster

### Read-Only

- `all` (Attributes List) List of all firewall rules (see [below for nested schema](#nestedatt--all))

<a id="nestedatt--all"></a>
### Nested Schema for `all`

Read-Only:

- `cluster_id` (Number) ID of the cluster
- `id` (Number) ID of the cluster
- `source_address` (String) Source address of allowed traffic

