# text2imageWebKubernetesConfig
text2imageWebKubernetesConfig:


build:
kustomize build overlays/dev | sed "s/:IMAGE_TAG/:0.0.2/" > overlays/dev/manifest/manifest.yaml

service port-forward:
kubectl -n text2image port-forward svc/text2image-front-service 9000:8080
ArgoCD:
kubectl -n argocd port-forward svc/argocd-server 8080:80