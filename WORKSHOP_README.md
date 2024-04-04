# Educates Workshop Repo
This repo contains the source configuration for an Educates workshop.

# Docs to help extend and build the workshop
For documentation, read the extensive docs at: https://docs.educates.dev/


# Publishing the content of your workshop
First download the educates CLI which can be done by following the doc here: https://docs.educates.dev/getting-started/quick-start-guide#downloading-the-cli
  
  
Now you can run a command to publish the contents to an OCI registry and generate the final manifest.  
Make sure to replace the image registry and path to meet your requirements:  

```bash
educates publish-workshop --image-repository=harbor.vrabbi.cloud/library --export-workshop="./resources/rendered-workshop-manifest.yaml"
```
  
# Deploying the workshop
```bash
kubectl apply -f resources/rendered-workshop-manifest.yaml
kubectl apply -f resources/training-portal.yaml
```
