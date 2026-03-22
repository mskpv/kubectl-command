kubectl get pod -n istio-system --show-labels

kubectl create namespace istio-playground

kubectl label namespace istio-playground istio-injection=enabled

The istio-injection=enabled label tells Istio to automatically inject sidecar proxies to all pods deployed in this namespace.

kubectl get pods -n istio-playground -w 

# means:
kubectl get pods → Lists all pods
-n istio-playground → Targets the istio-playground namespace
-w → Watch mode (continuously streams updates in real-time)



openssl s_client -connect auth.docker.io:443 -showcerts </dev/null 2>/dev/null | sed -n '/BEGIN CERTIFICATE/,/END CERTIFICATE/p' > ~/.config/certs/proxy-ca.pem 

zsh: is a directory: /Users/Prabhuraj.Murugesan/.config/certs/proxy-ca.pem
