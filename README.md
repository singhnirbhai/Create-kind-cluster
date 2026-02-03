# Step 1 — Prerequisites:

* Docker (running)

* kubectl

* kind

# Step 2 — The cluster spell:
```bash
vi kind-3node-cluster.yaml
```
```
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
  - role: control-plane
  - role: worker
  - role: worker
```
# Step 3 — Ignite the cluster

```bash
kind create cluster --name dev-cluster --config kind-3node-cluster.yaml
```
# Step 4 — Verify (trust nothing, verify everything)
```bash
kubectl get nodes
```
# Check cluster context
```bash
kubectl config current-context
```
# Install docker from docker official website 
```
https://docs.docker.com/engine/install/rhel/
```
# Install kubectl from official website
```
https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/
```
# Install kind tool
```
https://kind.sigs.k8s.io/docs/user/quick-start
```
