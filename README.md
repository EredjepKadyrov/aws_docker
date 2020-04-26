# aws_docker


## Makefile Creation Recap
Let’s recap the key concepts of creating a Makefile.

* setup: You have seen most of this line before, which is dealing with our Python 3 virtual environment.

* install: This installs the requirements for our environment. In our case, it also install the pytest and pylint libraries used later on in the Makefile.

* test: This is broken into two parts for testing.

** First, it will use .py files in the tests directory. The -vv flag ensures short test durations are still shown (see documentation), while the -cov flag helps to calculate what the test coverage of the code is (see documentation) in a given directory.

** The second line is used to test Jupyter Notebook cells. The --nbval flag makes pytest pay attention to jupyter notebooks (see documentation).

* lint: This will lint what is in the myrepolib directory, as well as the cli.py and web.py files in our current directory (see video). The --disable=R,C is used to disable the "convention" (C) and "refactor" (R) message classes (see related Stack Overflow post).

* all: You may notice this line looks a little different than the above lines, with the commands on the same line. This will execute our install, lint and test commands.

for this project was used materials from: 
https://github.com/EredjepKadyrov/DevOps_Microservices
