# PHP App

## Building container image

```bash
export CONTAINER_IMAGE_REGISTRY=594081136085.dkr.ecr.eu-north-1.amazonaws.com
export IMAGE_TAG=0.0.1
```

```bash
docker build -t ${CONTAINER_IMAGE_REGISTRY}/php-app:${IMAGE_TAG} .
```

## Pushing container image to registry

```bash
export CONTAINER_IMAGE_REGISTRY=594081136085.dkr.ecr.eu-north-1.amazonaws.com
export IMAGE_TAG=0.0.1
```

```bash
aws ecr get-login-password | docker login --username AWS --password-stdin ${CONTAINER_IMAGE_REGISTRY}
docker push ${CONTAINER_IMAGE_REGISTRY}/php-app:${IMAGE_TAG}
```