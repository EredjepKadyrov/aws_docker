# aws_docker


## Makefile Creation Recap
Let’s recap the key concepts of creating a Makefile.

* setup: You have seen most of this line before, which is dealing with our Python 3 virtual environment.

* install: This installs the requirements for our environment. In our case, it also install the pytest and pylint libraries used later on in the Makefile.

* test: This is broken into two parts for testing.

     * First, it will use .py files in the tests directory. The -vv flag ensures short test durations are still shown (see    
     documentation),      while the -cov flag helps to calculate what the test coverage of the code is (see documentation) in a given
     directory.

     * The second line is used to test Jupyter Notebook cells. The --nbval flag makes pytest pay attention to jupyter notebooks (see     
      documentation).

* lint: This will lint what is in the myrepolib directory, as well as the cli.py and web.py files in our current directory (see video). The --disable=R,C is used to disable the "convention" (C) and "refactor" (R) message classes (see related Stack Overflow post).

* all: You may notice this line looks a little different than the above lines, with the commands on the same line. This will execute our install, lint and test commands.


This repository provides the supporting material for the "ND9991 Cloud DevOps Nanodegree - C3 - Build CI/CD Pipelines, Monitoring, and Logging" course. This repo has two more branches, other than the master branch. 


### Blue/Green deployment strategy
* Blue/Green branch corresponds to the Blue/Green deployment strategy. 
 

### Dependencies
##### 1. AWS account
You would require to have an AWS account to be able to build cloud infrastructure. Particularly, you will need to create S3 buckets, EC2 instances, and IAM users.

#### 2. Jenkins on Ubuntu VM
As a part of the project, you will need to install Jenkins and a few plugins to assist your requirements, as mentioned in the "Jenkins Pipelines on AWS --> Project Details" page in the classroom. 


for this project was used materials from: 
https://github.com/udacity/DevOps_Microservices
