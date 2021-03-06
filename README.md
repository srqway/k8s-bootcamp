# Kubernetes Bootcamp #

**Note: This is a condensed version of our 2-day bootcamp tailored for the 1 day K8S Hackfest. To learn about our intensive 2 day K8S bootcamp, send us a note at kubernetes@architech.ca**

[Copyright (c) 2019, Architech. All rights reserved.](./COPYRIGHT.md)

** Link to PDF version of the presentation for this bootcamp is [here](./Kubernetes_Hackfest.pdf) ** 

[Kubernetes (K8S)](https://kubernetes.io/docs/home/) is the industry standard for deploying, managing, operating container based distributed applications.  It is proven in the most demanding production environments in the world.  Internet scale companies such as Google, Netflix, EBay and many more depend on Kubernetes to quickly deploy applications and bring product to market faster.

In this bootcamp, we will cover all the essential concepts in Kubernetes. We will go through Kubernetes from the persective of two user personas.

- The Application Engineer that engineers the software solutions deployed to K8S.
- The Platform Engineer that provisions, configures and operates the platform (including cloud services, K8S, CI/CD, databases, message queues, caches, authentication providers, etc) that the Application engineers depends on to bring product to market.

We will deploy a microservice based [application](./todo-app/README.md) to K8S.  Using this reference application, we will learn K8S concepts in a more meaningful way - as if you were using K8S to deploy and manage a real application.  We will cover scenarios such as:

- Continuous Integration/Continuous Deployment
- Blue/Green deployments
- Auto-scaling your application to deal with peak traffic demand
- RBAC (Role Based Access Control) to ensure Production environments are isolated from Dev/Test and QA.
- Many more.

By the end of this bootcamp, you will learn the following K8S concepts:

- [Pods - the unit of deployment on K8S](https://kubernetes.io/docs/concepts/workloads/pods/pod-overview/)
- [Services - how service discovery works in K8S](https://kubernetes.io/docs/concepts/services-networking/connect-applications-service/)
- [Deployments - doing rolling updates, rollbacks, scaling out](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
- [Storage - managing durable state with volumes, persistance volumes and persistent volume claims](https://kubernetes.io/docs/concepts/storage/volumes/)
- [Secrets - externalizing secrets and passwords](https://kubernetes.io/docs/concepts/configuration/secret/)
- [ConfigMaps - externalizing configuration from your applications](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/)
- [Jobs](https://kubernetes.io/docs/concepts/workloads/controllers/jobs-run-to-completion/)
- [DaemonSets](https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/)
- [StatefulSets](https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/)
- [Ingress and Ingress Controllers - key to controlling how requests originating from outside the cluster is routed to your services](https://kubernetes.io/docs/concepts/services-networking/ingress/)
- [RBAC - locking down your K8S environment](https://kubernetes.io/docs/admin/authorization/rbac/)
- [Helm - packaging and deploying your application to K8S](https://docs.helm.sh/)

### Outline: ###

- [Kubernetes Architecture](./bootcamp/exercises/Architecture.md)
    - Key components and what role they serve
    - Key K8S resources and their purpose
    - Quick overview of Kubernetes networking
    - K8S as a dynamic platform and what that means
- [Setting up your environment](./bootcamp/exercises/setup.md)
- The Todo list microservices application overview
    - Deploying the application to K8S
    - Making a change and doing a rolling-update
    - Scaling out the application to deal with increased traffic
- [Pods](./pods/README.md) - the unit of deployment in K8S
    - Defining the manifest
    - What to consider when decomposing your application into pods
    - Health checks and CPU, Memory requests and limits
- [Services](./services/README.md) - How do pods find each other?
    - Exposing your pods as services
    - Using load-balancers and NodePorts to expose your pods to clients outside your cluster
    - Accessing services external to your cluster. e.g. Azure CosmosDB service
- [Deployments](./deployments/README.md) - Deployments enable you to perform rolling upgrades, rollback, and scale up/scale down your services.
- [Storage](./storage/README.md) - Volumes, Persistent Volumes, Persistence Volume Claims, Storage Classes.
- [ConfigMaps](./configmaps/README.md) - ConfigMaps enable you to define configuration that is accessible as environment variables, files in a volume or command line arguments.
- [Ingress](./ingress/README.md) - Customizing the routing your published services.
    - Deploying the nginx ingress controller
    - Configuring routing to different version of your services
- [RBAC - Role Based Access Control](./security/README.md) - Controlling access to your K8S cluster.
    - K8S authn/authr model
    - Roles and Role bindings
    - Integrating Azure AD for authn/authr
    - Creating custom roles and role bindings to only allow access to a specific namespace (e.g. qa or dev)
- [Introduction to Helm](./helm/README.md) - Package manager for K8S deployments.
    - What is it and why you need it
    - Deploying the Todo list application using Helm
    - Charts and templates
    - Sharing your charts
- Brief overview of other K8S tools and projects you should know about:
    - [Draft](https://github.com/Azure/draft) - Tool to help developers be productive building/testing applications on K8S
    - [Minikube](https://github.com/kubernetes/minikube) - Local single node K8S cluster for development and learning.

### Interesting Links ###

* [Why Kubernetes](https://apprenda.com/why-kubernetes/)
* [Large-scale cluster management at Google with Borg](https://research.google.com/pubs/pub43438.html)
* [Borg, Omega and Kubernetes](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/44843.pdf)
* [12 Factor Application Principles](https://12factor.net/)
* [Kubernetes Case Studies](https://kubernetes.io/case-studies/)

### Very Helpful Utilities ###

* [kube-ps1 - displays your current K8S context and namespace in your shell prompt!](https://github.com/jonmosco/kube-ps1)
* [kubens & kubectx - quickly set the working context/namespace!](https://github.com/ahmetb/kubectx)