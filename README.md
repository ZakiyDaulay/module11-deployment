# Reflection 1 #

## Logs Before and After Exposure

Before exposing:
`Started HTTP server on port 8080`
`Started UDP server on port 8081`

After exposing:
`Get /`
` Get /`
every HTTP requests is being received

## purpose of `-n` option in `kubectl get`
The -n flag means `--namespace`, which tells kubectl to operate in a specific namespace.
running `kubectl get pods` creates a resource with a default namespace. But if we ran `kubectl get pods 
-n kube-system` will show pods like `coredns`, `kube-apiserver-minikube` ,`metrics-server` because they're in the kube-system namespace.