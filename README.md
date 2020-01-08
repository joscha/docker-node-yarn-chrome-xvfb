Docker Node Yarn Chrome Xvfb, etc.
==================================

Docker image which has installed the following:
- Node
- Yarn
- Chrome
- Xvfb
- JDK 11
- AWS CLI
- jq
- build-essential
- dependencies for node-canvas
- git-lfs
- protoc
- unzip
- netcat

Also see [Docker Hub](https://hub.docker.com/r/canvadev/ci-docker-node-yarn-chrome-xvfb/).


## Releasing

```bash
git tag <YYYY-mm-dd>
git push --tags
docker build . # will give you a "Successfully built <hash>"
docker tag <hash> canvadev/ci-docker-node-yarn-chrome-xvfb:<YYYY-mm-dd>
docker login
docker push canvadev/ci-docker-node-yarn-chrome-xvfb:<YYYY-mm-dd>
```
