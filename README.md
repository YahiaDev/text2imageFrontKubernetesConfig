# text2imageWebKubernetesConfig
text2imageWebKubernetesConfig:


build:

kustomize build overlays/dev | sed "s/:IMAGE_TAG/:0.0.2-SNAPSHOT/" > overlays/dev/manifest/manifest.yaml
