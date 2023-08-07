## Running locally using Docker and Minikube (local Kubernetes)

### Requirements:

- Linux or MacOS
- [Docker Engine](https://docs.docker.com/engine/install/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [Kubectl](https://kubernetes.io/docs/tasks/tools/)
- [Skaffold](https://skaffold.dev/docs/install/)

#### How to setup:

- Clone this repository `git clone https://github.com/charisschomba/setup-kubernetes-localhost.git`
- Setup kubernetes cluster. 
    - `minikube start --profile custom`
    - `skaffold config set --global local-cluster true`
    - `eval $(minikube -p custom docker-env)`
#### Note
- For linux users start minikube with kvm driver

    - `minikube start --driver=kvm2 --profile custom`
    - `skaffold config set --global local-cluster true`
    - `eval $(minikube -p custom docker-env)`

  [KVM2 installation](https://phoenixnap.com/kb/ubuntu-install-kvm)
- Navigate to `setup-kubernetes-localhost` and run `skaffold dev` to configure deployments, pods and service in the kubernetes cluster.
- Edit hosts file to redirect posts.com to minikube ip.
- First get minikube ip by running `minikube ip`
- [Enable ingress controller](https://kubernetes.io/docs/concepts/services-networking/ingress/). `minikube addons enable ingress`
- Add this `[Minikube ip] posts.com`
- Open hosts file, `sudo nano /etc/hosts`
- Add this `[Minikube ip] posts.com`

  #### Testing
  - Navigate to the browser navigate to `posts.com`
  


