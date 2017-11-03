

# Git repository

https://github.com/anasdox/docker-phpwebbuilder

# Build a custom image

```
docker build -t phpwebbuilder \
    --build-arg PHP_VERSION=7.1 \
    --build-arg COMPOSER_VERSION=1.5.2 \
    --build-arg NODE_VERSION=8.9.0 \
    --build-arg YARN_VERSION=1.3.2 \
    .
```

```
docker build -t phpwebbuilder \
    --build-arg PHP_VERSION=7.1 \
    --build-arg COMPOSER_VERSION=1.5.1 \
    --build-arg NODE_VERSION=6.2.2 \
    --build-arg YARN_VERSION=1.2.1 \
    .
```
