# Aqua Scanner Playbook 

This playbook simplifies the integration of aqua scans into a workflow by wrapping the aqua scan api endpoints into a playbook.

## Features
- it can produce a webhook url to post to a rocket chat channel
- it can print results to stdout
- it can fail fast based on your custom rules on what you consider to be a failed scan

## Environment 

- `aqua_url: string`
- `aqua_username: string`
- `aqua_password: string`

