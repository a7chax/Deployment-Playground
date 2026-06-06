# 🚀 deployment-playground

A personal playground for learning and experimenting with modern deployment workflows, DevOps practices, containerization, and infrastructure.

## Purpose

This repository is intended for hands-on learning. The examples and configurations are designed to help understand how applications are built, containerized, and deployed.

Feel free to experiment, break things, and rebuild them.

---

## Getting Started

Clone the repository:

```bash
git clone https://github.com/a7chax/deployment-playground.git
cd deployment-playground
```

This repository contains various deployment-related practices, such as:

* Docker fundamentals
* Docker Compose
* Multi-stage builds
* Reverse proxies
* CI/CD workflows
* Networking
* Container optimization
* Infrastructure experiments

---

## Docker BuildKit

Docker provides two builders:

* **BuildKit** (modern builder)
* **Legacy Builder** (traditional builder)

In some examples, BuildKit is intentionally disabled for educational purposes.

### Why disable BuildKit?

Disabling BuildKit helps you:

* Understand the traditional Docker build process.
* Observe how Docker image layers are created.
* Follow older tutorials and examples.
* Compare the legacy builder with BuildKit.

> **Note:** BuildKit is recommended for production and modern workflows. In this repository, it may be disabled temporarily to better understand Docker fundamentals.

### Enable BuildKit

```bash
buildkit-on() {
  export DOCKER_BUILDKIT=1
  echo "BuildKit enabled"
}
```

### Disable BuildKit

```bash
buildkit-off() {
  export DOCKER_BUILDKIT=0
  echo "BuildKit disabled"
}
```

Verify the current setting:

```bash
echo $DOCKER_BUILDKIT
```

Output:

```text
1  # BuildKit enabled
0  # Legacy builder
```

---

## Learning Philosophy

This repository prioritizes understanding over convenience.

Some configurations may intentionally avoid advanced features or modern defaults so that the underlying concepts are easier to understand before moving on to more sophisticated tools and workflows.
