---
subcategory: "BigQuery"
description: |-
  A datasource to retrieve a list of datasets in a project.
---

# `google_bigquery_datasets`

Get a list of datasets in a GCP project. For more information see
the [official documentation](https://cloud.google.com/bigquery/docs)
and [API](https://cloud.google.com/bigquery/docs/reference/rest/v2/datasets/list).

## Example Usage

```hcl
data "google_bigquery_datasets" "datasets" {
  project = "my-project"
}
```

## Argument Reference

The following arguments are supported:

* `project` - (Optional) The ID of the project in which the resource belongs.
  If it is not provided, the provider project is used.

## Attributes Reference

The following attributes are exported:

* `datasets` - A list of all retrieved BigQuery datasets. Structure is [defined below](#nested_datasets).

<a name="nested_datasets"></a>The `datasets` block supports:

* `labels` - User-provided dataset labels, in key/value pairs.
* `friendly_name` - The friendly name of the dataset.
* `dataset_id` - The id of the dataset.
* `location` - The geographic location of the dataset.
