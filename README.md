
# Description

This image contains most commons dependency managers used to build php applications

# Build a custom image

To build a custom image with diffrents versions of composer or nodejs or ... you can use docker build args

```
docker build -t phpwebbuilder \
    --build-arg PHP_VERSION=7.1 \
    --build-arg COMPOSER_VERSION=1.5.2 \
    --build-arg NODE_VERSION=8.9.0 \
    --build-arg YARN_VERSION=1.3.2 \
    --build-arg PHPCS_VERSION=^3.2 \
    --build-arg PHPUNIT_VERSION=^7.0 \
    .
```

```
docker build -t phpwebbuilder \
    --build-arg PHP_VERSION=5.6 \
    --build-arg COMPOSER_VERSION=1.5.1 \
    --build-arg NODE_VERSION=6.2.2 \
    --build-arg YARN_VERSION=1.2.1 \
    --build-arg PHPCS_VERSION=^3.2 \
    --build-arg PHPUNIT_VERSION=^7.0 \
    .
```

# Usage

## Composer

```
docker run --rm \
    --user $(id -u):$(id -g) \
    --volume $PWD:/app \
    --workdir /app \
    anasdox/phpwebbuilder \
    composer install --prefer-dist --no-interaction --ignore-platform-reqs
```

## NPM
```
docker run --rm \
    --user $(id -u):$(id -g) \
    --volume $PWD:/app \
    --workdir /app \
    anasdox/phpwebbuilder \
    npm install
```
