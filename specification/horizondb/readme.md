# Microsoft HorizonDb Management API

This directory contains the TypeSpec specification for the Microsoft HorizonDb Management API.

## Basic Information

These are the global settings for the HorisonDb API.

```yaml
title: HorizonDbManagementClient
description: The Microsoft HorizonDb Management API provides Azure Resource Manager operations for managing HorizonDb clusters, pools, replicas, and firewall rules.
openapi-type: arm
tag: package-horizondb-2026-01-20-preview
```

### Tag: package-horizondb-2026-01-20-preview

These settings apply only when `--tag=package-horizondb-2026-01-20-preview` is specified on the command line.

````yaml $(tag) == 'package-flexibleserver-2025-08-01'
input-file:
  - Microsoft.DBforPostgreSQL/stable/2025-08-01/openapi.json

## File Structure

``` yaml
specification/horizondb/
├── readme.md                           # This file
├── resource-manager/
│   └── Microsoft.HorizonDb/
│       └── preview/
│           └── 2026-01-20-preview/     # Generated OpenAPI specifications
└── HorizonDb.Management/               # TypeSpec source files
    ├── main.tsp                        # Main TypeSpec file with resource definitions
    ├── models.tsp                      # Data models and property definitions
    ├── routes.tsp                      # ARM resource operation interfaces
    ├── tspconfig.yaml                  # TypeSpec compiler configuration
    ├── examples/                       # API operation examples
    │   └── 2026-01-20-preview/         # Examples for the current API version
    ├── preview/                        # Generated OpenAPI output (local)
        └── 2026-01-20-preview/
````

## Compilation

To compile the TypeSpec specification:

```bash
cd specification/horizondb/HorizonDb.Management
npx tsp compile .
```

This will generate:

- OpenAPI 3.0 specifications in the `tsp-output/@azure-tools/typespec-autorest/resource-manager/Microsoft.HorizonDb/` directory
- Local preview files in the `preview/2026-01-20-preview/` directory
- SDK generation configuration for multiple languages (Python, Java, TypeScript, Go, .NET)

## Examples

The `examples/2026-01-20-preview/` directory contains JSON examples for all API operations, including:

- Cluster creation, retrieval, listing, and deletion
- Pool management within clusters
- Read replica operations
- Firewall rule configuration

Each example includes the required `operationId` and `title` fields for proper integration with the TypeSpec autorest emitter.
