# OSISM release 3.0.0

## Features

* OpenStack client container image in version Yoga is available
* Ansible >=2.10.0,<2.11.0 required by all Ansible collections
* Homer is now available as an initial dashboard
* For Keycloak the available MariaDB Galera cluster can now be used as database
  backend
* Zuul is now available as a new service for future deployment management
* OpenStack images for Kubernetes Cluster API (CAPI) version 1.22 are available
* Tailscale (https://tailscale.com) is available as an alternative for Wireguard
  on the testbed
* For Nova, SPICE is now supported as a console in addition to NoVNC
* A prepared machine image for the installation of the manager node is available
* Workers were switched to Celery with Redis as broker and backend
* Use of own NetBox image with pre-installed plugins
* Flower, a dashboard for Celery, was added as a service on the manager
* In the testbed, all hostnames were changed to publicly resolvable entries (``testbed.osism.xyz``)

## Removals

* Support for Zabbix has been removed, Prometheus will be used as the only
  monitoring stack in the future
* Heimdall as a service was removed, as an alternative Homer is now available

## Deprecations

* Cockpit is deprecated in favor of Boundary by HashiCorp

## Conformance

* Tests for OpenStack Powered Compute 2020.11 successful for Wallaby (https://refstack.openstack.org/#/results/054e85a0-857e-49c5-906c-3e124a1fdd03)
* OSISM is officially OpenStack Powered and listed in the marketplace (https://www.openstack.org/marketplace/distros/distribution/osism/osism)
* Designate and Heat are now also tested for Wallaby

## Fixes

* In the inventory reconciler the import into the NetBox was fixed
* The image of patchman was changed to Ubuntu to fix problems when using libapt
* In Patchman, Ubuntu 20.04 was added as a distribution

## Infrastructure

* An Elasticsearch service is now available for integration into the CI
* A Kibana service is now available for the evaluation of the logs from the CI
* A new Minio service is available for binary artifacts like machine images
* Plusserver provides resources on the Pluscloudopen for daily deployments
* It is now possible to set the permissions of all repositories in the osism
  organisation via the github-permissions repository