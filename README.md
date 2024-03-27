# App Definition & Delivery
## Build, CI/CD
* **Helm** : The Kubernetes Package Manager
* **ArgoCD** : Kubernetes-native tools to run workflows, manage clusters, and do GitOps right.
  
## DB
* **TiKV** : distributed transactional key-value database at large scale
* **Vitess** : a database clustering system for horizontal scaling of MySQL through generalized sharding
* **etcd** : used for configuration and service discovery in distributed systems like Kubernetes (optimized for read-heavy workloadss)

# Runtime
* **Rook** : cloud-native storage orchestrator for `Kubernetes`, providing the platform, framework, and support for Ceph storage to natively integrate with Kubernetes
* **Cilium** : efficiently route and manage network traffic at the application layer (Layer 7)
  * Encryption, Load-balancing, Network Policy, Networking(IPv4/6, Overlay, BGP, Egress Gateway)
* **Harbor** : cloud native registry project that stores, signs, and scans content


# Orchestration & Management
* **Kubernetes** : system for automating deployment, scaling, and management of containerized applications
* **Keda** : Kubernetes-based Event Driven Autoscaling component. It provides event driven scale for any container running in Kubernetes
* **Crossplane** : framework for building cloud native control planes without needing to write code
* **Envoy** : cloud-native high-performance edge/middle/service proxy
* **Istio** : simplify observability, traffic management, security, and policy with the Istio service mesh.
* **CoreDNS** : extensible DNS server that can serve as the Service Discovery layer in a variety of environments, including cloud-native deployments managed by Kubernetes

# Automation & Configuration
* **Terraform** : provision and manage cloud infrastructure or when working with immutable infrastructure principles
* **Ansible** : configuration management, software provisioning, and application deployment
  * Terraform can be used to provision the servers and other infrastructure components, and then Ansible can be used to configure those systems, install software, and ensure that they are in the desired state.
 
# Observability
Logging is more focused on capturing events and messages for retrospective analysis, debugging, and monitoring purposes. Tracing focuses on tracking the flow of requests or transactions in distributed systems to understand interactions and diagnose performance issues.

## Visualization
* Elasticsearch + Kibana
* **Grafana** for Prometheus
* Backstage

## Metrics
* **Prometheus** + **Cortex**
* **OpenMetrics** : standardized way to expose and collect metric data

## Log Collecting
* **Fluentd**
* **OpenTelemetry** : set of APIs, libraries, agents, and instrumentation that provide an end-to-end observability framework for collecting, processing, and exporting telemetry data, including metrics, traces, and logs.
  * For logs, use `OpenTelemetry`'s logging API to send log data to `Fluentd`
  * For metrics, use `OpenTelemetry`'s `Prometheus` exporter to expose metrics
* **Beats** + **Logstash**

## Tracing
* **Jaeger**

# Security
* **Falco** : cloud native runtime security tool
* **OpenPolicyAgent** : you define rules that govern how your system should behave
* **CertManager** : Automatically provision and manage TLS certificates in Kubernetes
* **Trivy** : Check OS packages and software dependencies in use (SBOM), Known vulnerabilities (CVEs), IaC issues and misconfigurations, Sensitive information and secrets, Software licenses (targeted on Container Image, Filesystem, Git Repository (remote), Virtual Machine Image, Kubernetes, AWS)
* **Hashicorp Vault** : A tool for secrets management, encryption as a service, and privileged access management

# References
* [google msa demo][gmsa-demo]

[gmsa-demo]: https://github.com/GoogleCloudPlatform/microservices-demo?tab=readme-ov-file
