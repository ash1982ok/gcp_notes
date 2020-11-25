# from console

To enable an API for a project using the console:

Go to the Cloud Console API Library.
From the projects list, select the project you want to use.
In the API Library, select the API you want to enable. If you need help finding the API, use the search field and/or the filters.
On the API page, click ENABLE.

# from gcloud SDK

https://cloud.google.com/sdk/gcloud/reference/services/enable

```text
gcloud services enable [SERVICE …] [--async] [GCLOUD_WIDE_FLAG …]
```

To see a list of available services for a project, run:
```text
gcloud services list --available
```

# from service API

https://cloud.google.com/service-usage/docs/reference/rest/v1/services/enable

Enable a service so that it can be used with a project.

*** HTTP request ***
POST https://serviceusage.googleapis.com/v1/{name=*/*/services/*}:enable

The URL uses gRPC Transcoding syntax.
