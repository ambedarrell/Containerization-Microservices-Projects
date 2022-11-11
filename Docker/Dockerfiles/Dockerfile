#FROM defines the base image
FROM ubuntu:latest
#USER is used to define the user that would execute RUN, CMD, ENTRYPOINT
USER root
#RUN is used to manage dependencies, softwares and packages
RUN apt-get update -y
RUN apt-get install apache2 -y
### LABELS are used to define app metadata
LABEL app-name="webapp" 
LABEL environment="dev" 
ENV project-name ssc-svcd
#ENTRYPOINT is used to start the application at runtime
#You can either use ENTRYPOINT or CMD
ENTRYPOINT [ "apachectl -D FORCEGROUND" ]
