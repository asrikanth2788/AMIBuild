# AMIBuild

This repo is to build an AMI with packer and ansible 

## Assumptions

1. aws_access_key and aws_secret_access_key values are added to the file ~/.aws/credentials
2. export aws_access_key and aws_secret_access_key values. (packer uses env values)
3. packer is already installed in the machine where you are running this build
4. you own a source image "ubuntu/images/hvm-ssd/ubuntu-focal-20.04-amd64-server*". If not, then you will be prompted to subscribe to that image from aws-marketplace

## Usage:

### checkout this git repo
```
1. git clone git@github.com:asrikanth2788/AMIBuild.git
2. cd AMIBuild
```
### Run packer command to build AMI with 
`3. packer build -var 'aws_access_key=SKFJALTJNCALKJT' -var 'aws_secret_key=adfagsgshsfgadrfag' -var 'owner=1234567890' template.json
