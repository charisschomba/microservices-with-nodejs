## Running locally using Docker and Minikube (local Kubernetes)

### Requirements:

- [Docker Engine](https://docs.docker.com/engine/install/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [Kubectl](https://kubernetes.io/docs/tasks/tools/)
- [Skaffold](https://skaffold.dev/docs/install/)

#### How to setup:

- Clone this repository `https://github.com/charisschomba/microservices-with-nodejs-demo.git`
- Navigate to microservices-with-nodejs-demo and run `skaffold dev` to configure deployments, pods and service in the kubernetes cluster.
- Edit hosts file to redirect posts.com to minikube ip.
- First get minikube ip by running `minikube ip`
- [Edit hosts windows](https://www.hostinger.com/tutorials/how-to-edit-hosts-file)
- Add this `[Minikube ip] posts.com`
- Linux/MacOS, open hosts file, `sudo nano /etc/hosts`
- Add this `[Minikube ip] posts.com`

  #### Testing
  - Navigate to the browser navigate to `posts.com`
  


