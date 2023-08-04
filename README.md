# k8s-tools
Miscellaneous tools for use with K8S

## chns
Changes the current working namespace without changing the context.

## pns
Prints the current working namespace (for use with chns).

## podroot
Connects to a pod (as root) in the working namespace (assumes that you're using chns from above).  Requires a pod name as an argument.  Assumes key-based SSH access to (and sudo configures on) worker nodes.  Note: this needs improvement before it can do things like: 
```
k get pod -o name|sed -e 's/^pod\///'|xargs podroot
```
It almost works.
