# pvc-k8-sample
Sample project explaining persistence volume and  persistence volume claim on K8 cluster with local path with node affnity

ssh into ur worker node and create a /mnt/data directory:
sudo mkdir /mnt/data
In the /mnt/data directory, create an index.html file:
sudo sh -c "echo 'Hello from Kubernetes storage' > /mnt/data/index.html"

# ssh into master node run
1. kubectl apply -f sample-volume.yaml
2. kubectl apply -f sample-volume-claim.yaml
3. kubectl apply -f sample-pod.yaml
# Enter into the pods shell
1. kubectl exec -it pv-pod bash
2. root@pv-pod:/# apt-get update
3. root@pv-pod:/# apt-get install curl
4. root@pv-pod:/# curl localhost
