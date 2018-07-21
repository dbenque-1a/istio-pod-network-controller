Istio Pod Network Controller
========================

Controller to manage Istio Pod Network

## Prerequisites

The following are required for the project

* OpenShift Command Line Tool
* OpenShift Account with _cluster-admin_ privileges
* Anisble (Installation)

## Installation

Clone Repository

```
mkdir -p $GOPATH/src/github.com/sabre1041
cd $GOPATH/src/github.com/sabre1041
git clone https://github.com/sabre1041/istio-pod-network-controller.git
cd istio-pod-network-controller
```

Login to OpenShift Environment

```
oc login https://<MASTER_API>
```

Run Ansible Galaxy to retrieve dependencies

```
ansible-galaxy install -r requirements.yml --roles-path=galaxy
```

Deployment

```
ansible-playbook -i ./inventory galaxy/openshift-applier/playbooks/openshift-cluster-seed.yml
```
