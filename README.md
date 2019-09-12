# k8s-cheatsheet
Collection of neat commands &amp; scripts for working with Kubernetes (K8S)

List all pods in specific namespace:

`kubectl get pods -n <namespace>`

Tail logs of specific pod:

`kubectl logs -f <pod>
`

Get all running pods with a specific label:

`kubectl get pods -l <label-key>:<label-value> --field-selector=status.phase=Running -o jsonpath="{.items[0].metadata.name} -n <namespace>`


Establish port-forwarding on localhost to specific pod:

`kubectl port-forward <pod> <local-port>:<pod-port>
`
`kubectl port-forward <pod> <port>
`

Delete pod:

`kubectl delete pod <pod>
`
