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