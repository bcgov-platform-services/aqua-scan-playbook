# Aqua Scanner Playbook 
[![Aqua Trivy Vulnerability Scanner](https://github.com/bcgov-platform-services/aqua-scan-playbook/actions/workflows/trivy.yaml/badge.svg)](https://github.com/bcgov-platform-services/aqua-scan-playbook/actions/workflows/trivy.yaml)
This playbook simplifies the integration of aqua scans into a workflow by wrapping the aqua scan api endpoints into a playbook.

## Playbooks

- `scan_entire_registry`: This will scan all the registires configured in the var `image_registries: string[]`. **Only accounts with the correct scope may scan entire registries**
> coming soon
> - `scan_image`: This will scan image(s) in a registry, wait for the results, and report them

## Environment 

- `aqua_url: string`
- `aqua_username: string`
- `aqua_password: string`
- `image_registries: string[]`

## Building Image

The image is managed via github release. On Release a github workflow builds and publishes a docker image into the bcdevopscluster dockerhub account. 

## Running Image

`docker run bcdevopscluster/aqua-scan-playbook ansible-playbook scan_entire_registry.yaml -e aqua_username="..." -e aqua_password="..."`

