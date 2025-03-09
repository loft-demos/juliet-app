# Using Flux with vCluster Platform

By enabling the installation of Flux, the resulting vCluster Platform demo environment will include:
- apps:
  - Flux Operator - includes Flux `ResourceSets` 
  - [Flux2](https://fluxcd.io/flux/) - and, yes, we are using Argo CD to install Flux, please don't judge
- manifests -
  - The [Capcitor UI](https://github.com/gimlet-io/capacitor), a UI for Flux
  - A vCluster Platform `VirtualClusterTemplate` resource to be used to create one of the `VirtualClusterInstances` below
  - A vCluster Platform Bash `App` that can be used with `VirtualClusterInstances` to create a Flux KubeConfig `Secret` in a vCluster Platform host or connected cluster when running a single instance of Flux
  - A Flux `GitRepository` for this reposiotry and mapped to the **Auth Core** vCluster Platform Project namespace - `p-auth-core`
  - A Flux `Kustomization` resource that will create the `VirtualClusterInstance` resources defined under the [kustomize directory](./kustomize)
- pull-request-environments - example of dynamic provision of vCluster instances for ephemeral Pull Request environments with Flux
  - A Flux Operator `ResourceSetInputProvider` configured for GitHub Pull Requests
  - A Flux Operator `ResourceSet` that:
    - Uses a `Kustomize` Flux resource to provision Pull Request specific `VirtualClusterInstances`
    - 
