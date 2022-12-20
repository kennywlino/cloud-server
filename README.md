# LAB - CLASS 16

## Project: Cloud Servers on AWS

## Author: Kenny W. Lino

## Problem Domain

In this lab, we begin to work with various AWS services. We start with using Elastic Beanstalk to deploy a simple Node.js server to EC2 both via the AWS Control Panel GUI and via the Elastic Beanstalk terminal tool.

## Deployment Process

### GUI

In order to deploy via the GUI, we went to the [Elastic Beanstalk section](https://us-west-2.console.aws.amazon.com/elasticbeanstalk/home?region=us-west-2#/welcome) and clicked "Create Application". From there, we filled out some basic info like 'Application Name' and 'Platform' and uploaded a .zip folder containing our server.js and package.json files. Afterwards, we clicked 'Create Application' and this deployed our app.

### Terminal

In order to deploy via the terminal for the very first time, we need to set our access key under 'Users > Access Keys' in the Identity and Access Management (IAM) tab. Our user will also need "AdministratorAccess-AWSElasticBeanstalk" under their permissions. After we have our Access Key, we can run `aws configure` in the terminal. There, we will be asked things like the Access Key ID and Key, and we can put the info in there. Everything else can be set to the default values.

After the configuration is set up, we can use `eb init` within the folder we'd like to upload to start the set up for our project. With `eb create`, we can actually create our EB instance. This command will ask a few questions like environment name and DNS CNAME prefix, which we can adjust to our choosing. The load balancer type will be 'Application'.

### Links and Resources

- [Server deployed via GUI](http://simple-aws-server-env.eba-s267ckwk.us-west-2.elasticbeanstalk.com/)
- [Server deployed via terminal](http://simple-aws-server-terminal-dev.us-west-2.elasticbeanstalk.com/)

### Setup

#### How to initialize/run your application

### Features / Routes

- `/` -- Displays a hello world message

### Tests

No tests.

#### UML