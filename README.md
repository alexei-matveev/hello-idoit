#### Experiments with i-doit in k3s

Assuming you already installed the Token in your local config:

    $ export KUBECONFIG=~/.kube/config
    $ kubectl get nodes
    $ source <(kubectl completion bash)

Install i-doit [images](https://github.com/bheisig/i-doit-docker) in
Kubernetes

    $ kubectl create namespace hello-idoit
    $ kubectl config set-context --current --namespace=hello-idoit
    $ kubectl apply -k k3s/

Then visit the [URL](https://idoit.localhost).
