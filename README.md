# Konductor
## Cloud Developer & Operator Bastion Container

Konductor is as a multi-function operator and developer bastion.
Included:
- Fish Shell
- uor-client-go
- VS Code Server
- Starship prompt by starship.rs
- TTYd Terminal Server
- SSH Server
- SSH
- Tmux
- Helm
- Kumactl
- Kubectl
- VirtCtl
- GRPCurl
- Pulumi
- Skopeo
- Jq
- Yq

![Konductor](./.github/images/Konductor.png)

## Install:
- [Helm](https://github.com/containercraft/konductor#helm-beta)
- [Podman](https://github.com/containercraft/konductor#podman)
- Docker
- Docker Compose

### [Helm (beta)](https://github.com/ContainerCraft/helm/tree/main/charts/konductor)

### Podman

#### Podman Play Kube:
````bash
podman play kube -f kube.yaml
````

#### Podman Run:
````bash
podman run -d --rm --pull=always \
    --name konductor \
    --hostname konductor \
    --cap-add=CAP_AUDIT_WRITE \
    --security-opt label=disable \
    --publish 2222:2222 \
    --publish 7681:7681 \
    --publish 8088:8080 \
  ghcr.io/containercraft/konductor
````
