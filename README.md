# Install Artifactory in Amazon Linux2 ec2 instance.

## Pre-requisites:
create an linux ec2 instance with the following
    - T2.small
    - Open port 8081---->in the security group
    - Install Java

## Install Java
    yum install java-1.8* -y 

## Download Artifactory packages onto /opt/
    For Latest version of Artifactory OSS download it from here https://jfrog.com/open-source/
    For Older version of Artifactory OSS download it from here https://jfrog.bintray.com/artifactory/
    For Latest version of Artifactory Pro download it from here https://jfrog.com/artifactory/

## Extract artifactory tar.gz file
    cd /opt 
    wget https://jfrog.bintray.com/artifactory/jfrog-artifactory-oss-6.9.6.zip
    unzip jfrog-artifactory-oss-6.9.6.zip

## Start the services
    cd /opt/artifactory-oss-6.9.6/bin
    ./artifactory.sh start

## Access artifactory from browser
    http://<PUBLIC_IP_Address>:8081 

## Credentials
    username: admin
    passord: password
