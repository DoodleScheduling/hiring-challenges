# DevOps Challenge

In order to test your skills and knowledge, as well as to give you an idea of how we work end-to-end, we ask you to complete the following challenge.  

## Summary

This challenge includes setting up [Keycloak IAM](https://www.keycloak.org/guides#getting-started) (Identity Access and Management) with Infinispan caching system. This represents a simplified version of our own authentication system which involves using a high availability caching system. The authentication service (Keycloak) persists user sessions within Infinispan, using it as a remote store for the session entries.

We are looking for a solution deployed on a Kubernetes cluster. You are free to choose which Kubernetes cluster you are testing with (we recommend a local kind of cluster).

The final solution we would like to see, is a Git repository with all necessary Kubernetes resources used for your IAM solution. It is up to you what kind of delivery method you choose (vanilla Kubernetes resources, `kustomization`, `helm`, `jsonnet`, …).

## What we expect

- Deploy Keycloak and a separate Infinispan to a local Kubernetes cluster
- Connect Keycloak to a database (you are free to choose how you do that)
- Create at least one distributed Keycloak cache on the remote infinispan and configure Keycloak to connect to it. Other Keycloak caches can be distributed on the embedded Infinispan.
- Be prepared to explain the reasoning behind the choices you have made, especially for the preexisting resources you used. We value people who understand how things work and this is reflected in their implementations.
- Make sure to declare the parts of the solution that you imported from an existing source, if you did use it
- Test your solution and make sure your deliverables are functioning
- Document your solution properly. It’s very important for us that you provide something that is understandable to others
- Submit your solution in a Git repository (You can choose the Git provider)

We expect that you do **not spend more than 8 hours** over a time span of one week on this challenge.

Even if you do not meet all expectations, please send in your solution!

## Solution output

A ready to deploy solution for Kubernetes, with all required Keycloak and Infinispan manifests, declared in a Git repository, which fulfills the expectations mentioned above.

## Nice to have

- Configure authentication for the remote Infinispan caches
- Configure custom Infinispan logging (enable debug mode for some components and/or all)
- Add a custom provider https://github.com/aerogear/keycloak-metrics-spi and deploy it to the Keycloak server
- Expose Keycloak for access outside of your cluster
