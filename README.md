## Quickstart: Setting Up Your Learning Environment

### 1. Install Task

First, you need to install Task on your system. Please follow the official installation guide for your operating system:

**[Official Task Installation Guide](https://taskfile.dev/installation/)**

For most Linux and macOS users, the following command will work:
```bash
sh -c "$(curl --location https://taskfile.dev/install.sh)" -- -d -b /usr/local/bin
```

### 2. Set Up Your Kubernetes Environment

Once Task is installed, you can set up your entire local Kubernetes environment with a single command. This will install `docker`, `kind`, and `kubectl`.

Open your terminal in the root of this project and run:```bash
task setup-kube
```
> **Note for Podman Users:** If you prefer to use Podman instead of Docker, you can specify it as the container engine on the command line like this:
> ```bash
- task setup-kube CONTAINER_ENGINE=podman
- ```

### 3. Manage Your Local Kubernetes Cluster

The Taskfile also includes simple commands to create and destroy your Kubernetes cluster. The cluster will be created using the `kind-config.yaml` file in this repository.

*   **To start your cluster:**
    ```bash
    task cluster-up
    ```

*   **To shut down and delete your cluster:**
    ```bash
    task cluster-down
    ```

### 4. List All Available Commands

To see a full list of all available commands and their descriptions at any time, run:
```bash
task --list
```