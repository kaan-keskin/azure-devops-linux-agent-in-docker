
Login on BUILDAH

$ buildah login docker.io


Build Docker Image in BUILDAH

$ buildah build --no-cache -t azuredevops-linux-test-agent-auth-negotiate:2.153.1 -f Dockerfile.testagent .

$ buildah tag localhost/azuredevops-linux-test-agent-auth-negotiate:2.153.1 docker.io/keskinkaan/azuredevops-linux-test-agent-auth-negotiate:2.153.1


List Images in BUILDAH

$ buildah images


Push Docker Image to Docker Hub

$ buildah push docker.io/keskinkaan/azuredevops-linux-test-agent-auth-negotiate:2.153.1


