# snippits
code snippits from Kuberneties 

Delete all Errored namespaces in Kuberneties
kubectl delete pod `kubectl get pods --namespace kube-system | awk '$3 == "Error" {print $1}'` --namespace kube-system

Error registering network: failed to configure interface flannel.1: link has incompatible addresses.
sudo ip link delete flannel.1

sudo kubeadm init fails at timeout

sudo sed -i 's/failureThreshold: 8/failureThreshold: 20/g' /etc/kubernetes/manifests/kube-apiserver.yaml
docker kill apiserver name

delete a deployment group
kubectl delete -n <NAMESPACE> deployment <DEPLOYMENTNAME>
