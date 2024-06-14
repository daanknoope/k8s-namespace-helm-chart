# k8s-namespace-helm-chart
A Helm chart for creating Kubernetes namespaces - making it easy to manage namespaces using GitOps.

## Adding the repository to helm
```sh
helm repo add namespace-chart-repo https://daanknoope.github.io/k8s-namespace-helm-chart/
helm repo update
```
## Example values file
```yml
namespaces:
  - name: my-namespace
    labels:
      foo: bar
      key: value
```

## Installing the helm chart with custom namespaces
```sh
helm install namespaces namespace-chart-repo/namespace-chart --values example.yml
```