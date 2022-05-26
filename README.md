# SQUER Brainfood Session | ArgoCD
https://argo-cd.readthedocs.io/en/stable/

This repository contains the presented examples from the SQUER internal Brainfood Session in May 2022.
It gives a gentle introduction to ArgoCD, lists some interesting reads and might help getting started with a GitOps approach.

## Prerequisites
+ k3d installed (https://k3d.io/)

## Local Setup

Execute the following command to create a new k8s (k3d) cluster and install ArgoCD

``make bootstrap``

Running ``kubectl get pods -A`` shows you all the pods running on your newly created cluster. As soon as a pod in namespace
``argocd`` starting with the name ``argocd-server-*`` is in status ``Running``, you can execute the following command to access the
argocd-ui:

``make argo-ui``

This allows you to access the argo-ui at https://localhost:8080 . The username is per default ``admin`` and the password can be 
retrieved via ``make show-password``

