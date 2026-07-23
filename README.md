# Cloud MySQL service for Kubernetes on Wodby

Connect Wodby Kubernetes applications to an externally managed Cloud MySQL
service.

This repository defines the Wodby service manifests and operational
configuration for Cloud MySQL.

- [Browse Wodby services](https://wodby.com/services)
- [Wodby service documentation](https://wodby.com/docs/2.0/services/)
- [Service manifest reference](https://wodby.com/docs/2.0/services/template/)

## Wodby stacks using this service

- [Cloud MySQL application stack](https://github.com/wodby/stack-cloud-mysql)
- [Drupal application stack](https://github.com/wodby/stack-drupal)
- [Laravel application stack](https://github.com/wodby/stack-laravel)
- [WordPress application stack](https://github.com/wodby/stack-wordpress)

## Service overview

| Property | Manifest configuration |
| --- | --- |
| Service name | `cloud-mysql` |
| Type | Database; external connection with no in-cluster workload |
| Versions | `5.5` by default; also available: `5.6`, `5.7`, `8` |
| Configuration | 1 generated or fixed tokens |

## Use this service

Use this service through one of the Wodby application stacks listed above, or
reference `cloud-mysql` from a custom Wodby stack.

A service is a reusable component and does not deploy by itself. The stack
defines its links, settings, versions, resources, and relationship to the rest
of the application.

## Maintain a custom version

1. Fork this repository.
2. Edit the service manifest and referenced files.
3. Import the repository as a [Git-backed service](https://wodby.com/docs/2.0/services/create/#create-a-git-backed-service).
4. Reference the service from a stack manifest.

Keep service, workload, container, endpoint, link, volume, config, and
derivative names stable unless dependent stacks and app-level overrides are
updated at the same time.

Validate the manifests with:

```bash
wodby service validate-manifest service.yml --org <org-id>
```

See the [service manifest reference](https://wodby.com/docs/2.0/services/template/) and the [managed services index](https://github.com/wodby/services).
