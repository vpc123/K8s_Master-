# K8s_Master- 设置节点可以调度


### 前提：使用kubeadm部署k8s集群


#### Kubernetes是Google大神开源的容器管理组件，常被称为K8s (PS：K表示第一个字母，s表示最后一个字母，8表示中间一共有8个字母:) ). 被Docker的使用者用于Docker服务的编排和管理。虽然Docker家出了Swarm用来管理Docker，但是目前来看，使用K8s的仍然居多。



#####  使master节点可以调度pod


默认情况下，master节点不能被调度启动pod，如果需要将master节点加入到调度中，需要执行以下命令:

    $kubectl taint nodes --all node-role.kubernetes.io/master-



总结：使得k8s集群中master节点可以调度，针对资源不足我们需要使得master节点可以调度。

