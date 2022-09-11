[![Build Stable](https://github.com/frappe/frappe_docker/actions/workflows/build_stable.yml/badge.svg)](https://github.com/frappe/frappe_docker/actions/workflows/build_stable.yml)
[![Build Develop](https://github.com/frappe/frappe_docker/actions/workflows/build_develop.yml/badge.svg)](https://github.com/frappe/frappe_docker/actions/workflows/build_develop.yml)

Everything about [Frappe](https://github.com/frappe/frappe) and [ERPNext](https://github.com/frappe/erpnext) in containers.

# Getting Started

To get started, you need Docker, docker-compose and git setup on your machine. For Docker basics and best practices. Refer Docker [documentation](http://docs.docker.com).
After that, clone this repo:

```sh
git clone https://github.com/frappe/frappe_docker
cd frappe_docker
```

### Try in Play With Docker

<a href="https://labs.play-with-docker.com/?stack=https://raw.githubusercontent.com/frappe/frappe_docker/main/pwd.yml">
  <img src="https://raw.githubusercontent.com/play-with-docker/stacks/master/assets/images/button.png" alt="Try in PWD"/>
</a>

Wait for 5 minutes for ERPNext site to be created or check `create-site` container logs before opening browser on port 8080. (username: `Administrator`, password: `admin`)

# Development

We have baseline for developing in VSCode devcontainer with [frappe/bench](https://github.com/frappe/bench). [Start development](development).

This project uses a Jenkinfile to Deploy the following;

1. Checkout codebase from the repository
2. Build Helm chart and Push to helm repository
3. Deploy to a Kubernetes Cluster
4. Setup FluxCD on GitOps
5. Create a Kustomization and a source file
6. Clean up resources

# Requirement for Development(Kubernetes)

1. Kubernetes Clusters
2. Github Environment
3. Linux Instance(you should be able ssh into the instance and gain access to the Kubernetes clusters)
4. Jenkins
5. Kustomize
6. Kompose
7. Docker & Docker compose