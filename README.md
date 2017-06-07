# Upsource PSI Agent with tools

This project contains a sample Dockerfile that declares extended Upsource PSI Agent docker image with additional tools used for source code processing.

Extended Upsource PSI Agent docker image is inherited from `jetbrains/upsource-psi-agent` and contains the following tools:
- nodejs (latest stable v6.x), 
- yarn (latest stable)
- PHP5 (latest stable)
- Python 2.7.9 (it is a part of base image `openjdk:8`) 

For building the image you need to perform the following:

1. Choose version of base [jetbrains/upsource-psi-agent](https://hub.docker.com/r/jetbrains/upsource-psi-agent/tags/) 
(let it be referred as `<version>` below)

2. `docker pull jetbrains/upsource-psi-agent:<version>`

3. Replace `@VERSION@` in Dockerfile with an actual chosen `<version>` of base image [jetbrains/upsource-psi-agent](https://hub.docker.com/r/jetbrains/upsource-psi-agent/tags/)  

4. Run the docker build command:
`docker build -t upsource-psi-agent-with-tools`