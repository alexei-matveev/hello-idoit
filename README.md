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

#### I-doit API

The API is not included, sigh.  See the
[issue](https://github.com/bheisig/i-doit-docker/issues/6).  And you
need to register to download it, dont even ask if one can redistribute
it with a custom image, IANAL.  That and the docs advising against
direct SQL updates & inserts. So pick your battles.
