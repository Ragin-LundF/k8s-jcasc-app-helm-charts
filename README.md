# k8s-jcasc App Example Chart Repository

This repository contains helm charts for the k8s-jcasc example.

More information:
- Medium Article [Kubernetes and CI/CD — How to integrate in your development process](https://ragin.medium.com/kubernetes-and-ci-cd-how-to-integrate-in-your-development-process-9b483b194975)
- Github [k8s-JCasC-Mgmt tool](https://github.com/Ragin-LundF/k8s-jcasc-management-go)
- Github [k8s-JCasC-Mgmt example project](https://github.com/Ragin-LundF/k8s-jcasc-mgmt-example)
- Github [k8s-JCasC-app-example](https://github.com/Ragin-LundF/k8s-jcasc-app-example)
- Github [k8s-JCasC docker containers](https://github.com/Ragin-LundF/k8s-jenkins-docker)
- Github [k8s-JCasC helm charts example](https://github.com/Ragin-LundF/k8s-jcasc-app-helm-charts)
- Github [k8s-JCasC helmfile deployment example](https://github.com/Ragin-LundF/k8s-jcasc-deploy-helmfile-example)

# How to add a new chart version

In the parent directory of the helm chart:

```bash
helm package <chartname>
helm repo index .
```

Then add the `index.yaml` and the `.tgz` file to this repository.

To use the repository as helm repository, it needs to be added with:

```bash
helm repo add reddotrepo 'https://github.com/Ragin-LundF/k8s-jcasc-app-helm-charts/main/reddot'
helm repo update
```

Now the chart should be available:

```bash
helm search reddot
```