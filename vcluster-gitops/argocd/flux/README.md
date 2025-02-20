# Using Flux with vCluster Platform

By enabling the installation of Flux, the resulting vCluster Platform demo environment will include:
- Flux2
- The Capcitor UI
- A Flux `GitRepository` for this reposiotry and mapped to the **Auth Core** vCluster Platform Project namespace - `p-auth-core`
- A Flux `Kustomization` resource that will create the `VirtualClusterInstance` resources defined under the [kustomize directory](./kustomize)
