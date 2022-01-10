# Azure DevOps Linux Agent OCI Image Creation Steps

## Login with DOCKER / BUILDAH

```shell
$ docker login -u username -p password docker.io
```

```shell
$ buildah login -u username -p password docker.io
```

## Build OCI Image in DOCKER / BUILDAH

```shell
$ docker build -t azuredevops-linux-test-agent-auth-negotiate:2.170.1 -f Dockerfile.testagent.negotiate .

$ docker build -t azuredevops-linux-agent-auth-negotiate:jdk17-jdk11-jdk8-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.170.1 -f Dockerfile.superagent.negotiate .
```

```shell
$ buildah build -t azuredevops-linux-test-agent-auth-negotiate:2.170.1 -f Dockerfile.testagent.negotiate .

$ buildah build -t azuredevops-linux-agent-auth-negotiate:jdk17-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.170.1 -f Dockerfile.superagent.negotiate .
```

## Tag OCI Image in DOCKER / BUILDAH

```shell
$ docker tag azuredevops-linux-test-agent-auth-negotiate:2.170.1 docker.io/scopeinfra/azuredevops-linux-test-agent-auth-negotiate:2.170.1

$ docker tag azuredevops-linux-agent-auth-negotiate:jdk17-jdk11-jdk8-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.170.1 docker.io/scopeinfra/azuredevops-linux-agent-auth-negotiate:jdk17-jdk11-jdk8-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.170.1
```

```shell
$ buildah tag localhost/azuredevops-linux-test-agent-auth-negotiate:2.170.1 docker.io/scopeinfra/azuredevops-linux-test-agent-auth-negotiate:2.170.1

$ buildah tag localhost/azuredevops-linux-agent-auth-negotiate:jdk17-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.170.1 docker.io/scopeinfra/azuredevops-linux-agent-auth-negotiate:jdk17-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.170.1
```

## List Images in DOCKER / BUILDAH

```shell
$ docker images
```

```shell
$ buildah images
```

## Push Images to Docker Hub in DOCKER / BUILDAH

```shell
$ docker push docker.io/scopeinfra/azuredevops-linux-test-agent-auth-negotiate:2.170.1

$ docker push docker.io/scopeinfra/azuredevops-linux-agent-auth-negotiate:jdk17-jdk11-jdk8-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.170.1
```

```shell
$ buildah push docker.io/scopeinfra/azuredevops-linux-test-agent-auth-negotiate:2.170.1

$ buildah push docker.io/scopeinfra/azuredevops-linux-agent-auth-negotiate:jdk17-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.170.1
```
