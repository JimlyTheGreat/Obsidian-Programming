---
last-modified: 2023-09-13
tags:
  - kubernetes
---
## API Version
---
> [!quoteno]
> The api version of a resource is specific to the resource you are targeting. When specifying an api version with 'apiVersion: ~version~' it tells kubernetes which version of the specific resource to use. Then kubernetes will use that version when applying the resource to a cluster. 

#### Common API Versions

> [!quoteno]
> `apps/v1`: For Deployments, StatefulSets, and DaemonSets.
> `v1`: For Pods, Services, and ConfigMaps.
> `networking.k8s.io/v1`: For NetworkPolicies and Ingress.

## Metadata
---
> [!quoteno]
> Meta data is exactly what it sounds like. It is just more information related to the particular resource that will be applied.

#### Name

> [!quoteno]
> The `name` under metadata uniquely identifies a resource within a namespace. It serves as a "handle" for interacting with the resource.

#### Namespace

> [!quoteno] 
> The `namespace` is an optional field. When omitted, the resource is assumed to belong to the 'default' namespace. Namespaces are a way to divide cluster resources between multiple users and are a cornerstone for RBAC (Role-Based Access Control).

#### Labels

> [!quoteno]
> Key-value pairs attached to resources for filtering and selection.

## Spec
---
> [!quoteno]
> The `spec` (specification) outlines the desired state for the resource. This can include a wide array of settings and configurations, such as `replicas` for Deployments or `ports` for Services.

#### Replicas

> [!quoteno]
> The desired number of identical pods to be running. If not specified, defaults to 1.

#### Selector

> [!quoteno]
> Specifies how to find pods that match a certain criteria. Used for both deployments and services for routing traffic to pods.

#### Ports

> [!quoteno]
> Defines the ports that the container exposes. This is generally just the same end result as what you would normally do in Docker for a given container.

#### Volume Mount

> [!quoteno]
> Specifies what volumes should be mounted to a container.
