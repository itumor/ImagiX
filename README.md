# ImagiX
Intelligent AI-based container image updater that proactively senses updates, analyzes security vulnerabilities, and integrates smoothly into GitOps for effortless automation.

# download kubebuilder and install locally.
curl -L -o kubebuilder "https://go.kubebuilder.io/dl/latest/$(go env GOOS)/$(go env GOARCH)"
chmod +x kubebuilder && sudo mv kubebuilder /usr/local/bin/

# Initialize Your Project
Navigate to your working directory and run the following command to initialize a new Kubebuilder project:

kubebuilder init --domain imagix.myk8soperator.com --repo github.com/itumor/ImagiX

# Create an API
kubebuilder create api --group intelligentimageupdater  --version v1 --kind IntelligentImageUpdater

make manifests


# Install kubectl (Kubernetes CLI)

# Download the latest release
curl -LO "https://dl.k8s.io/release/$(curl -sL https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

# Make it executable
chmod +x kubectl

# Move to system path
sudo mv kubectl /usr/local/bin/

# Verify installation
kubectl version --client

# 2. Install k3s (Lightweight Kubernetes by Rancher)

# Install via script
curl -s https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash

# Create a cluster
k3d cluster create mycluster

# Test
kubectl get nodes

