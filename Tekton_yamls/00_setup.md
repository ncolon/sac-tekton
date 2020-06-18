# Project setup

Create a namespace

```
oc new-project sac-tekton
```

Install Tekton Dashboard
```
oc new-project tekton-pipelines
```

Install the Tekton Dashboard (OpenShift only)
```
kubectl apply --filename https://github.com/tektoncd/dashboard/releases/download/v0.6.1.4/openshift-tekton-dashboard-release.yaml --validate=false
```

Install Tekton Webhook

NOTE: Update the WEBHOOK_CALLBACK_URL with your clusters sub-domain

```
kubectl apply --filename https://github.com/tektoncd/dashboard/releases/download/v0.6.1.4/openshift-tekton-webhooks-extension-release.yaml 
```

Get the route to access the UI

```
kubectl get route tekton-dashboard -n openshift-pipelines
```


Create Personal Access Token

```
enable repo and admin: repo_hook permissions

```
