
## Login on BUILDAH

```shell
$ buildah login -u username -p password docker.io
```

## Build OCI Image in BUILDAH

```shell
$ buildah build --no-cache -t azuredevops-linux-test-agent-auth-negotiate:2.153.1 -f Dockerfile.testagent.negotiate .
$ buildah build --no-cache -t azuredevops-linux-agent-auth-negotiate:jdk17-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.153.1 -f Dockerfile.superagent.negotiate .
```

## Tag OCI Image in BUILDAH

```shell
$ buildah tag localhost/azuredevops-linux-test-agent-auth-negotiate:2.153.1 docker.io/scopeinfra/azuredevops-linux-test-agent-auth-negotiate:2.153.1
$ buildah tag localhost/azuredevops-linux-agent-auth-negotiate:jdk17-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.153.1 docker.io/scopeinfra/azuredevops-linux-agent-auth-negotiate:jdk17-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.153.1
```

## List Images in BUILDAH

```shell
$ buildah images
```

## Push Images to Docker Hub in BUILDAH

```shell
$ buildah push docker.io/scopeinfra/azuredevops-linux-test-agent-auth-negotiate:2.153.1
$ buildah push docker.io/scopeinfra/azuredevops-linux-agent-auth-negotiate:jdk17-mvn3.8-nodejs16-py3-go1.17-dockercli-buildah-sonarscanner4.6-azp2.153.1
```

