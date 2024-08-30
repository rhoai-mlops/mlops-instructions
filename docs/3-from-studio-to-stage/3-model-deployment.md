## Model Deployment via GitOps

We deployed our `jukebox` model in experiment environment manually, but for the higher environments we need to store the definitions in Git and deploy our models via Argo CD to get all the benefits that GitOps brings.

# Deploying Jukebox 

1. In your code server IDE, open `mlops-gitops/values.yaml` file and **swap** `enabled: false` to `enabled: true` as shown below for each of the app-of-pb definitions:

    <div class="highlight" style="background: #f7f7f7">
    <pre><code class="language-yaml">
        # Test App of Apps for Models
        - name: model-deployments
          enabled: true
          source_path: "."
          helm_values:
            - test/values.yaml
        # Staging App of Apps for Models
        - name: model-deployments
          enabled: true
          source_path: "."
          helm_values:
            - stage/values.yaml
    </code></pre></div>