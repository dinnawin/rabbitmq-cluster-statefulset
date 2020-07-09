# rabbitmq-cluster-statefulset

## Deploy HA RabbitMQ in Kubernetes

- rabbitmq-configmap.yaml
- rabbitmq-rbac.yaml
- rabbitmq-service-ext.yaml
- rabbitmq-service.yaml
- rabbitmq-statefulset-pvc.yaml
- rabbitmq-statefulset.yaml

## 集群对外访问

由于官方给出的解决方案中，使用hostname作为自动识别主机的节点名，而此时，statefulset必须设置为 headless service .  如果要让 rabbitmq 暴露出端口 ，对外访问。 

这里使用对同一个 statefulset 新增 Nodeport 形式的service。 


