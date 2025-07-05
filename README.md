# Prompt Engineering
Create a set of Kubernetes manifests using AI Chatbots.

This file contains a collection of prompts that can be used with AI chatbots to generate Kubernetes manifest files.

| NAME | PROMPT | DESCRIPTION | EXAMPLE |
|---|---|---|---|
| Application Pod | Create a Kubernetes Pod manifest. App name should be kbot. Use ghcr.io/vadym-marchenko/telebot.git:v1.0.1-linux-arm64 image. save it to the app.yaml file in yaml directory. | Creates an application pod | /yaml/app.yaml | 
| kbot Deployment | Create Deployment for kbot pod. expose via port 80, it should have 2 replicas save it to deployment.yaml | Creates a Kubernetes Deployment for the kbot application with 2 replicas. | /yaml/deployment.yaml |
| kbot Service | Expose kbot deployment via loadbalancer service | Creates a LoadBalancer Service to expose the kbot deployment externally. | /yaml/service.yaml |
| Data Pipeline Job | create job manifest that will execute datapipline using the following commandline code ... | Creates a Kubernetes Job to run a data pipeline using the local DirectRunner. | /yaml/app-job.yaml |
