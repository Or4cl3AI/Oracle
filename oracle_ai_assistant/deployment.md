```python
# oracle_ai_assistant/deployment.py

import os
import subprocess

def build_docker_image(image_name, dockerfile_path):
    """
    Build a Docker image using the specified Dockerfile.
    """
    subprocess.run(["docker", "build", "-t", image_name, "-f", dockerfile_path, "."])

def push_docker_image(image_name, registry):
    """
    Push a Docker image to the specified container registry.
    """
    subprocess.run(["docker", "push", f"{registry}/{image_name}"])

def deploy_kubernetes_manifest(manifest_path):
    """
    Deploy a Kubernetes manifest file.
    """
    subprocess.run(["kubectl", "apply", "-f", manifest_path])

def scale_kubernetes_deployment(deployment_name, replicas):
    """
    Scale a Kubernetes deployment to the specified number of replicas.
    """
    subprocess.run(["kubectl", "scale", "deployment", deployment_name, "--replicas", str(replicas)])

def create_kubernetes_service(service_name, port, target_port):
    """
    Create a Kubernetes service.
    """
    subprocess.run(["kubectl", "create", "service", "nodeport", service_name, "--tcp", f"{port}:{target_port}"])

def create_kubernetes_ingress(ingress_name, host, service_name, service_port):
    """
    Create a Kubernetes ingress.
    """
    subprocess.run(["kubectl", "create", "ingress", ingress_name, "--rule", f"{host}/*={service_name}:{service_port}"])

# Example usage
if __name__ == "__main__":
    # Build Docker image
    build_docker_image("oracle-ai-assistant", "Dockerfile")

    # Push Docker image to container registry
    push_docker_image("oracle-ai-assistant", "registry.example.com")

    # Deploy Kubernetes manifest
    deploy_kubernetes_manifest("kubernetes/deployment.yaml")

    # Scale Kubernetes deployment
    scale_kubernetes_deployment("oracle-ai-assistant", 3)

    # Create Kubernetes service
    create_kubernetes_service("oracle-ai-assistant-service", 80, 8080)

    # Create Kubernetes ingress
    create_kubernetes_ingress("oracle-ai-assistant-ingress", "example.com", "oracle-ai-assistant-service", 80)
```
