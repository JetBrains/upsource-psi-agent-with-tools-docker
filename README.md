# upsource-psi-agent-with-tools-docker

This project contains the Dockerfile and all necessary scripts to build the Docker image of jetbrains/upsource-psi-agent with additional tools used for source code processing.
This Dockerfile MAY be used as an example for building your own images inherited from jetbrains/upsource-psi-agent with those particular tools required for your projects.

Image described by sample Dockerfile is inherited from jetbrains/upsource-psi-agent and contains the following tools:
- nodejs (latest stable v6.x), 
- yarn (latest stable)
- PHP5 (latest stable)
- Python 2.7.9 (it is a part of base image openjdk:8) 

Before building the image one should define an actual version of base image jetbrains/upsource-psi-agent in Dockerfile instead of parameter @VERSION@