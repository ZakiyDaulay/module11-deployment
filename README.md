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

# Reflection 2 #

## What is the difference between Rolling Update and Recreate deployment strategy?

Rolling update gradually replaces old pods with new ones, while recreate terminates all existing pods

## Try deploying the Spring Petclinic REST using Recreate deployment strategy and document your attempt.


I modified the `deployment.yml` file to use and changed the type under `strategy`  from `rollingUpdate` to `Recreate`. Then I deleted the old deployment file and 
reapplied the new one. 

## Prepare different manifest files for executing Recreate deployment strategy.
I created the `deploymentrecreate.yml` file

## The benefits of using Kubernetes manifest files?

Using manifest files is very reusable, as it can be reused for redeployment and across different environments.

It also reduces human error compared to manual commands

It's also very good for documentation, as it acts as a self-documenting code for our infrastructure. 