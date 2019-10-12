# MiniKube - Install

Minikube is single K8s cluster for testing/dev purpose

## Minikube requires docker 

### Ubuntu / Debian
```bash
sudo apt-get update && \
    sudo apt-get install docker.io -y
```
### CentOS / RedHat
```bash
sudo yum install -y yum-utils \
  device-mapper-persistent-data \
  lvm2
sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
sudo yum install docker-ce docker-ce-cli containerd.io
```

## Installing Minikube

```bash
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
```
### Checking Version

```bash
minikube version
```

## Kubectl

Kubectl is a command line interface for running commands against Kubernetes clusters.

## Installing

The kubectl version has to be within one minor version difference of the Kubernetes cluster. For example, a v1.2 client should work with v1.1, v1.2, and v1.3 master.

Kubectl can be installed on Ubuntu, Debian, CentOS, RedHat operating systems.

### Ubuntu / Debian

```bash
sudo apt-get update && sudo apt-get install -y apt-transport-https
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
```

### CentOS / RedHat

```bash
cat <<EOF > /etc/yum.repos.d/kubernetes.repo
[kubernetes]
name=Kubernetes
baseurl=https://packages.cloud.google.com/yum/repos/kubernetes-el7-x86_64
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://packages.cloud.google.com/yum/doc/yum-key.gpg https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg
EOF
yum install -y kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
```

For further information about kubectl installation method, please refer to [the Kubernetes documentation.](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

## Minikube Start
```bash
minikube start --vm-driver=none
```
## Minikube status

```bash
minikube status
host: Running
kubelet: Running
apiserver: Running
kubectl: Correctly Configured: pointing to minikube-vm at 10.128.0.6
```
## Minikube Stop and Delete

```bash
minikube stop
minikube delete
```

### Installation of Minikube with kvm2 driver -- If you want install with a VM drive!

### Installation of minikube

 - Apparently installation from snap doesn't work as expected, use curl for installation of the latest version.
 - `curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64`

 - `sudo install minikube-linux-amd64 /usr/local/bin/minikube`
 
### Installation of kvm2

##### Install dependencies and configure user groups

 - `sudo apt install libvirt-clients libvirt-daemon-system qemu-kvm libvirt-bin`
 - `sudo usermod -a -G libvirt $(whoami)`
 - `newgrp libvirt`

##### kvm2 installation
 - `curl -LO https://storage.googleapis.com/minikube/releases/latest/docker-machine-driver-kvm2 && sudo install docker-machine-driver-kvm2 /usr/local/bin/`


### Start minikube
 - `minikube start --vm-driver=kvm2`
 
 ## Sample Minikube run
 
 ```bash
 kubectl run hello-minikube --image=gcr.io/google_containers/echoserver:1.4 --port=8080
 kubectl expose deployment hello-minikube --type=NodePort
 kubectl get services
 ```
 
 [K8s Cheatsheet](/cheatsheet.md)
