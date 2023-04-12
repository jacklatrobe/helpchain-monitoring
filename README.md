# Helpchain Monitoring

The `helpchain-monitoring` repository provides components and configurations to enable monitoring of a Kubernetes cluster and an AI language model solution hosted on that cluster. The project manages the setup of monitoring and logging for the HelpChain service hosted on Kubernetes.

## Kubernetes

Kubernetes, often abbreviated as “K8s,” automates the scheduling, scaling, and maintenance of containers in any infrastructure environment. First open sourced by Google in 2014, Kubernetes is now part of the Cloud Native Computing Foundation.

Just like a conductor directs an orchestra, telling the musicians when to start playing, when to stop, and when to play faster, slower, quieter, or louder, Kubernetes manages your containers—starting, stopping, creating, and destroying them automatically to reflect changes in demand or resource availability. Kubernetes automates your container infrastructure via:
- Container scheduling and auto-scaling
- Health checking and recovery
- Replication for parallelization and high availability
- Internal network management for service naming, discovery, and load balancing
- Resource allocation and management

The HelpChain service is hosted on Kubernetes. 

## DataDog

Datadog is an observability service for cloud-scale applications, providing monitoring of servers, databases, tools, and services through a SaaS-based data analytics platform. Datadog’s integrations with Kubernetes, Docker, containerd, etcd, Istio, and other related technologies are designed to tackle the considerable challenges of monitoring orchestrated containers and services.

The Datadog Agent’s Kubernetes integration collects metrics, events, and logs from your cluster components, workload pods, and other Kubernetes objects. Integrations with container runtimes including Docker and containerd collect container-level metrics for detailed resource breakdowns. Wherever your Kubernetes clusters are running—including Amazon Web Services, Google Cloud Platform, or Azure—the Datadog Agent automatically monitors the nodes of your Kubernetes clusters. Datadog’s Autodiscovery and 600+ built-in integrations automatically monitor the technologies you are deploying. APM and distributed tracing provide transaction-level insight into applications running in your Kubernetes clusters.

## Components

The `helpchain-monitoring` repository includes the following components and configurations to enable monitoring of a Kubernetes cluster and an AI language model solution:

- `datadog-agent`: This is the Datadog Agent deployed as a DaemonSet on the Kubernetes cluster to monitor the nodes, components, and workloads of the cluster.

- `datadog-config`: This is the Datadog Agent configuration file with Kubernetes-specific settings.

- `datadog-secrets`: This is a Kubernetes secret that contains the API key for Datadog.

- `kube-state-metrics`: This is a Kubernetes service that provides metrics about the state of the Kubernetes cluster.

## Getting Started

To get started with monitoring your Kubernetes cluster and AI language model solution using the components in this repository, follow these steps:

1. Clone the repository to your local machine.

```
git clone https://github.com/<your-username>/helpchain-monitoring.git
```

2. Navigate to the cloned repository.

```
cd helpchain-monitoring
```

3. Update the `datadog-secrets` Kubernetes secret with your Datadog API key.

4. Deploy the components to your Kubernetes cluster.

```
kubectl apply -f .
```
