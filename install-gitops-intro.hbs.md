# Install Tanzu Application Platform (GitOps)

GitOps is an operational framework that uses Git repositories as a single source of truth. Under GitOps, you describe the desired state of a Tanzu Application Platform configuration using a declarative specification and place it in a Git repository.

<!-- TODO: this release is ready for production use in a specific set of conditions, review these conditions to see if your situation qualifies
  - general GitOps benefits/wants
  - if you want a simple instance and can store sensitive data encrypted ni your git repo ==> #SOPS
  - if you need to store secrest in external store blah blah... => #ESO
  
-->

To install Tanzu Application Platform on your Kubernetes clusters using GitOps:

## <a id='next-steps'></a> GitOps with sensitive data encrypted in hosted Git repo

|Step|Task|Link|
|----|----|----|
|1.| Review the prerequisites to ensure you have met all requirements before installing. |[Prerequisites](prerequisites.hbs.md)|
|2.| Accept Tanzu Application Platform EULAs and install the Tanzu CLI. |[Accept Tanzu Application Platform EULAs and installing the Tanzu CLI](install-tanzu-cli.hbs.md)|
|3.| Install Cluster Essentials for Tanzu*. |[Deploy Cluster Essentials](https://docs.vmware.com/en/Cluster-Essentials-for-VMware-Tanzu/{{ vars.url_version }}/cluster-essentials/deploy.html)|
|4.| Install Tanzu Application Platform. |[Install Tanzu Application Platform via Gitops](install-gitops-sops.hbs.md)
|5.| (Optional) Install any additional packages that were not in the profile. |[Install individual packages](install-components.hbs.md)|
|6.| Set up developer namespaces to use installed packages. |[Set up developer namespaces to use installed packages](set-up-namespaces.hbs.md)|
|7.| Install developer tools into your integrated development environment (IDE). |[Install Tanzu Developer Tools for VS Code](vscode-install-online.hbs.md)|






## <a id='next-steps'></a> GitOps with sensitive data stored in external store

<!-- ... "Supported on AWS Secrets Manager" ... -->


|Step|Task|Link|
|----|----|----|
|1.| Review the prerequisites to ensure you have met all requirements before installing. |[Prerequisites](prerequisites.hbs.md)|
|2.| Accept Tanzu Application Platform EULAs and install the Tanzu CLI. |[Accept Tanzu Application Platform EULAs and installing the Tanzu CLI](install-tanzu-cli.hbs.md)|
|x | --- reviewed to here --- | .. |
|3.| Create AWS Resources (EKS Cluster, roles, etc)|[Create AWS Resources](aws-resources.hbs.md)|
|4.| Install Cluster Essentials for Tanzu*. |[Deploy Cluster Essentials](https://docs.vmware.com/en/Cluster-Essentials-for-VMware-Tanzu/{{ vars.url_version }}/cluster-essentials/deploy.html)|
|5.| Add the Tanzu Application Platform package repository, prepare your Tanzu Application Platform profile, and install the profile to the cluster. |[Install the Tanzu Application Platform package and profiles](install-gitops-eso.hbs.md)|
|6.| (Optional) Install any additional packages that were not in the profile. |[Install individual packages](install-components.hbs.md)|
|7.| Set up developer namespaces to use installed packages. |[Set up developer namespaces to use installed packages](set-up-namespaces.hbs.md)|
|8.| Install developer tools into your integrated development environment (IDE). |[Install Tanzu Developer Tools for VS Code](vscode-install-online.hbs.md)|


\* _When you use a VMware Tanzu Kubernetes Grid cluster, there is no need to install Cluster Essentials because the contents of Cluster Essentials are already installed on your cluster._

After installing Tanzu Application Platform on to your Kubernetes clusters, proceed with [Get started with Tanzu Application Platform](getting-started.html).