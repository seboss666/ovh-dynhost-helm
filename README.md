# Helm chart for OVH DynHost

This is a little kubernetes cronjob to manage the [OVH DynHost service](OVH DynHost service).

## Deployment

You need to provide at least two parameters to the chart:

- the domain
- the credentials for the dynhost service (see OVH documentation for the details about these ones).

```bash
helm upgrade --install <release-name ovh-dynhost --set dynhost.domain=<domain> --set dynhost.credentials=<credentials> -n <namespace> --create-namespace
```