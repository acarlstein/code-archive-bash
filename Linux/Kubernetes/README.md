# Kubernetes Shortcuts for Docker Containers

The following are some bash commands I made on the rush to make my life easier when working with Kubernetes.
These files have the extension TXT to prevent any possible issues in downloading them.
Note: Only for Linux/Unix bash

* createtemp: Create a temporary deployment (with a pod) based on the name provided.
  * Equivalent to run: kubectl run -it –rm=true <name>–image=tutum/curl –namespace <environment>

* deldeploy: Delete deployment in environment.
  * Equivalent to run: kubectl –namespace=<environment> delete deployment <deployment name>

* descpod: Describe pod for specific environment.
  * Equivalent to run: kubectl –namespace=<environment> describe pods/<pod name>

* lsconfigmaps: List configmap(s) available based on environment provided.
  * Equivalent to run: kubectl –namespace=<environment> get configmaps

* lsdeploys: List deployments(s) based on environment provided.
  * Equivalent to run: kubectl –namespace=<environment> get deployments

* lspods: List pod(s) based on environment provided.
  * Equivalent to run: kubectl –namespace=<namespace> get pods

* podcp: Copy files from/to pod in an environment.
  * Equivalent to run: kubectl cp <source> <destination> <flags>

* podenv: Show pod environment variables.
  * Equivalent to run: kubectl –namespace=<environment> exec -it <pod name> env

* podlog: Show pod log.
  * Equivalent to run: kubectl logs <flags> <pod name> –namespace=<environment>

* podterm: Open a Shell for a pod in a specific environment.
  * Equivalent to run: kubectl –namespace=<environment> exec -it <pod name> sh

* restartpod: Restart pod in environment.
  * Equivalent to run: kubectl –namespace=<environment> delete pods/<pod name>

* showconfigmap: Show specific configmap based on specific environment.
  * Equivalent to run: kubectl –namespace=<environment> get configmaps/<pod name> -o=yaml

* shpod: Run a command line in the pod’s shell.
  * Equivalent to run: kubectl exec <pod name> –namespace=<environment> — <command line(s)>
