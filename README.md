# Local Deployment

This script is designed to manage and deploy services on Minikube. It provides a comprehensive set of features to deploy individual services or groups, manage CI/CD configurations, and deploy or remove specific tools.

## Prerequisites

- Ensure that you have Minikube installed and configured on your system.
- Install the necessary Python packages, including `google-cloud-storage`, `kubernetes`, and `pyyaml`.

## Environment Variables

Before running the script, ensure the following environment variables are set:

- `BUILD_WORK_DIR`: Path to the build working directory.

## Usage

The script offers a series of global options and subcommands that allow flexible management of deployments, tools, and configurations.

### Global Options

These options can be used independently or in combination:

- `--build-test <service>`: Run build-test for a specific service.
- `--deploy <service>`: Deploy a specific service.
- `--deploy-group <group-name>`: Deploy all services within a specified group.
- `--tools <tool-name>`: Deploy specific tools to Minikube. Options include: `mongo`, `elastic`, `redis`, `istio`, `prometheus`, `all`.
- `--cicd <config-type>`: Deploy CI/CD related configurations to Minikube. Options include: `all`, `secret`, `configmap`.
- `--remove-tools <tool-name>`: Remove specific tools from Minikube. Options include: `mongo`, `elastic`, `redis`, `istio`, `prometheus`, `all`.

### Commands

Commands are standalone operations that can be executed independently of global options:

- `remove <service>`: Remove a specific deployed service.
- `stop`: Stop Minikube.
- `start`: Start Minikube.
- `reset`: Reset all Minikube components.

### Command Examples

Deploy a Service:

