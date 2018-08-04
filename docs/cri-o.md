cri-o
===============

cri-o is container developed by kubernetes project.
Currently, only basic function is supported for cri-o.

* cri-o is supported kubernetes 1.11.1 or later.
* helm and other feature may not be supported due to docker dependency.
* scale.yml and upgrade-cluster.yml are not supported.

helm and other feature may not be supported due to docker dependency.

Use cri-o instead of docker, set following variable:

#### all.yml

```
kubeadm_enable: true
...
download_container: false
```

#### k8s-cluster.yml

```
etcd_deployment_type: host
kubelet_deployment_type: host
manage_docker: false
manage_crio: true
```

