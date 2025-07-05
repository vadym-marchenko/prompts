# Prompt Engineering
Create a set of Kubernetes manifests using AI Chatbots.

This file contains a collection of prompts that can be used with AI chatbots to generate Kubernetes manifest files.

| NAME | PROMPT | DESCRIPTION | EXAMPLE |
|---|---|---|---|
| Application Pod | Create a Kubernetes Pod manifest. App name should be kbot. Use ghcr.io/vadym-marchenko/telebot.git:v1.0.1-linux-arm64 image. save it to the app.yaml file in yaml directory. | Creates an application pod | /yaml/app.yaml | 
| kbot Deployment | Create Deployment for kbot pod. expose via port 80, it should have 2 replicas save it to deployment.yaml | Creates a Kubernetes Deployment for the kbot application with 2 replicas. | /yaml/deployment.yaml |
| kbot Service | Expose kbot deployment via loadbalancer service | Creates a LoadBalancer Service to expose the kbot deployment externally. | /yaml/service.yaml |
| Data Pipeline Job | create job manifest that will execute datapipline using the following commandline code ... | Creates a Kubernetes Job to run a data pipeline using the local DirectRunner. | /yaml/data-pipeline.yaml |
| Liveness Probe App | create liveliness probe app using ghcr.io/vadym-marchenko/telebot.git:v1.0.1-linux-arm64 image with /healthcheck endpoint and save yaml in app-livenessProbe.yaml | Creates a Deployment for the kbot app with an HTTP liveness probe. | /yaml/app-livenessProbe.yaml |
| Readiness Probe App | create readyness probe app using ghcr.io/vadym-marchenko/telebot.git:v1.0.1-linux-arm64 image with /ready endpoint and save yaml in app-readinessProbe.yaml | Creates a Deployment for the kbot app with an HTTP readiness probe. | /yaml/app-readinessProbe.yaml |
| App with Volume | create app with volume mounted to /mnt/data using ghcr.io/vadym-marchenko/telebot.git:v1.0.1-linux-arm64 image and save yaml in app-volumeMounts.yaml | Creates a Deployment with an emptyDir volume mounted at /mnt/data. | /yaml/app-volumeMounts.yaml |
| NFS Backup CronJob | create cron job that will mount NFS network drives and exeute rsync... | Creates a CronJob to perform an rsync backup between two NFS volumes. | /yaml/app-cronjob.yaml |
| Multi-container Pod | create multicontainer pod that will use telebot.git:v1.0.1-linux-arm64 image and linux alpine image and save yaml to app-multicontainer.yaml file | Creates a Pod with a main application container and an Alpine Linux sidecar. | /yaml/app-multicontainer.yaml |
| App with Secret Env | create app that will get api key from environment secret using ghcr.io/vadym-marchenko/telebot.git:v1.0.1-linux-arm64 image with /ready endpoint and save yaml in app-secret-env.yaml | Creates a Deployment that mounts a Secret value as an environment variable. | /yaml/app-secret-env.yaml |
| App with Resources | create pod that will use telebot.git:v1.0.1-linux-arm64 image and will require the following resources cpu: 200m, memory: 123mb and and save yaml to app-resources.yaml | Creates a Pod with specified CPU and memory resource requests. | /yaml/app-resources.yaml |
