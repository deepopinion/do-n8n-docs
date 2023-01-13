---
description: Data collection and privacy in n8n.
---

# Data collection

n8n collects selected usage and performance data to help diagnose problems and improve the platform. n8n takes care to keep this data anonymous and to avoid collecting sensitive data. Read about how n8n stores and processes this information in the [privacy policy](https://n8n.io/legal/){:target=_blank .external-link}.

## What n8n collects

- Error codes and messages of failed executions (excluding any payload data, and not for custom nodes)
- Error reports for app crashes and API issues
- The graph of a workflow (types of nodes used and how they're connected)
- From node parameters:
    - The 'resource' and 'operation' that a node is set to (if applicable)
    - For HTTP request nodes, the domain, path, and method (with personal data anonymized)
- Data around workflow executions:
	- Status
	- The user ID of the user who ran the execution
	- The first time a workflow loads data from an external source
	- The first successful production (non-manual) workflow execution
- Workflow sharing data:
	- Workflow ID and user ID when a user opens the sharing modal
	- Workflow ID and user ID when a user removes a sharee
	- User attempts to save a locked workflow
- The domain of webhook calls, if specified (excluding subdomain).
- Details on how the UI is used (for example, navigation, nodes panel searches)
- Diagnostic information
    - n8n version
    - Selected settings:
        - DB_TYPE
        - N8N_VERSION_NOTIFICATIONS_ENABLED
        - N8N_DISABLE_PRODUCTION_MAIN_PROCESS
        - [Execution variables](/hosting/environment-variables/environment-variables/#executions)
        - N8N_BASIC_AUTH_ACTIVE
    - OS, RAM, and CPUs
    - Anonymous instance ID
 - IP address

## What n8n doesn't collect

n8n doesn't collect private or sensitive information, such as:

- Personally identifiable information (except IP address)
- Credential information
- Node parameters (except 'resource' and 'operation')
- Execution data
- Sensitive settings (for example, endpoints, ports, DB connections, username/password)
- Error payloads

## How collection works

Most data is sent to n8n as events that generate it occur. Workflow execution counts and an instance pulse are sent periodically (every 6 hours).

## Opting out of telemetry

Telemetry collection is enabled by default. To disable it you can configure the following environment variables.

To opt out of telemetry events:

```bash
export N8N_DIAGNOSTICS_ENABLED=false
```

To opt out of checking for new versions of n8n:

```bash
export N8N_VERSION_NOTIFICATIONS_ENABLED=false
```

See [configuration](/hosting/configuration/) for more info on how to set environment variables.

## Documentation telemetry

n8n's documentation (this website) uses cookies to recognize your repeated visits and preferences, as well as to measure the effectiveness of our documentation and whether users find what they're searching for. With your consent, you're helping us to make our documentation better.

[Change cookie settings](#__consent){ .md-button }


