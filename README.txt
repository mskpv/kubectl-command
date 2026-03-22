kubectl get pod -n istio-system --show-labels

kubectl create namespace istio-playground

kubectl label namespace istio-playground istio-injection=enabled

The istio-injection=enabled label tells Istio to automatically inject sidecar proxies to all pods deployed in this namespace.

kubectl get pods -n istio-playground -w 

# means:
kubectl get pods → Lists all pods
-n istio-playground → Targets the istio-playground namespace
-w → Watch mode (continuously streams updates in real-time)