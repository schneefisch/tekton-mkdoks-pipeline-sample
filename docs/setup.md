# Setup How To

## Prerequisites

### Repository

Create a repository for the documentation, e.g. on Github.
As an alternative, use an existing project or repository and create your documentation in a dedicated directory.

### Local Kubernetes

Install `kubectl` by running

    brew install kubectl

Verify the installation

    kubectl version --client

As a local kubernetes setup I am using [Rancher Desktop](https://rancherdesktop.io/).
Install "Rancher Desktop" on your machine.
After startup open "Preferences" -> "Kubernetes" and check "Enable Kubernetes". This may require a restart of the virtual machine.

To verify that Rancher Desktop is up and running, open the terminal and type

    kubectl cluster-info

this should show information on your local kubernetes cluster

```shell
Kubernetes control plane is running at https://127.0.0.1:6443
CoreDNS is running at https://127.0.0.1:6443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy
Metrics-server is running at https://127.0.0.1:6443/api/v1/namespaces/kube-system/services/https:metrics-server:https/proxy
```

install the tekton-cli

    brew install tektoncd-cli

### Setup Tekton

Install tekton inside the kubernetes cluster

    kubectl apply -f deploy/tekton-release.yaml

Apply the pipeline by running:

```shell
kubectl apply -f deploy/docs-pipeline.yaml
```
