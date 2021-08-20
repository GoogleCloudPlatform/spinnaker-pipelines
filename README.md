# Spinnaker pipeline templates

This repository contains the code used in the
[Canary rollout with Spinnaker and Istio]()
tutorial.

This tutorial describes how to set up a canary deployment pipeline using Spinnaker, Istio, Cloud Monitoring, and Kayenta. It’s intended for developers or operators who want to implement robust deployment strategies with Spinnaker. It also assumes you’re familiar with Kubernetes and Istio.
Spinnaker is an open source, continuous delivery system led by Netflix and Google to manage application deployment on various computing platforms, including App Engine, Google Kubernetes Engine (GKE), Compute Engine, AWS, and Azure. Using Spinnaker, you can implement advanced deployment methods, including canary deployments.

In a canary deployment, you expose a new version of your application to a small portion of your production traffic and analyze its behavior before full deployment. Doing so helps you mitigate risk. 
To use canary deployments, you must accurately compare the behavior of the old and new versions of your application. The differences can be subtle and might take some time to appear. You might also have many different metrics to examine. Read more about the canary pattern in Application deployment and testing strategies.

In this tutorial, you use a sampleapp application that has a configurable error rate. The configurable error rate lets you test the deployment pipelines. A deployment with a higher error rate, for example, can’t pass the canary analysis step and fails deployment.

