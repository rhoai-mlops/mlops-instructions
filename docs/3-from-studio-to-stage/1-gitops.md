## GitOps 

### OpenShift GitOps Basic Install
> Argo CD is one of the most popular GitOps tools. It keeps the state of our OpenShift applications synchronized with our git repos. It is a controller that reconciles what is stored in our git repo (desired state) against what is live in our cluster (actual state). We can configure Argo CD to take actions based on these differences, such as auto sync the changes from git to the cluster or fire a notification to say things have gone out of whack.

1. To get started, we've written a Helm Chart to deploy an instance of Argo CD to the cluster. On your terminal (in the IDE), add the redhat-cop helm charts repository. This is a collection of charts curated by consultants in the field from their experience with customers. Pull requests are welcomed :P

```bash
./helm repo add redhat-cop https://redhat-cop.github.io/helm-charts
```

```bash
cat << EOF > /tmp/argocd-values.yaml
ignoreHelmHooks: true
operator: []
namespaces:
  - <TEAM_NAME>-mlops
teamInstancesAreClusterScoped: false
argocd_cr:
  initialRepositories: |
    - url: https://<GIT_SERVER>/<TEAM_NAME>/mlops.git
      type: git
      passwordSecret:
        key: password
        name: git-auth
      usernameSecret:
        key: username
        name: git-auth
      insecure: true
EOF
```

```bash
helm upgrade --install argocd \
  --namespace <TEAM_NAME>-mlops \
  -f /tmp/argocd-values.yaml \
  redhat-cop/gitops-operator
```

```bash
echo https://$(oc get route argocd-server --template='{{ .spec.host }}' -n <TEAM_NAME>-ci-cd)
```

2. Deploy S3 via Argo CD UI in mlops namespace to get familiar with Argo CD (app of apps can come later ?)

