# Deploy the ConfigMap
kubectl create -f configmap.yaml

# Create POD with the env variable
kubectl create -f pod-cmd.yaml

# Check the logs
kubectl logs test-pod-cmd

# Create the POD with the env variable
kubectl create -f pod-env.yaml

# Check the env vars
kubectl exec -it test-pod-vol /bin/sh

# Create the POD with env vars
kubectl create -f pod-vol.yaml

# Check the logs
kubectl logs test-pod-vol

# Access the shell
kubectl exec -it test-pod-vol /bin/sh

#Check the files
cd /etc/config
cat log.level 
cat log.location
