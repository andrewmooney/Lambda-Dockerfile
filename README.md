# Building dependency packages for Lambda

### Container includes 
* Nodejs v6.10.0
* Python 2.7
* Python 3.6
* gcc-c++
* vim
* zip
* unzip
* NVM

When building a Lambda function it is sometimes necessary to pre build the Python and Nodejs modules using Amazon Linux.

This can either be done remotely on an EC2 instance or locally in a Docker container.

## Creating an Amazon Linux Docker container

Clone repo in to local directory.
```bash
git clone https://github.com/andrewmooney/Lambda-Dockerfile.git
```

In a terminal window navigate to the location of the Dockerfile and run the following command.
```bash
docker build --no-cache -t amazonlinux-lambda -f Dockerfile .
```

Once the build has completed run the follow= ing command to launch the container.
```bash
docker run -it amazonlinux-lambda
```

This should drop you in to the shell of the container.
```bash
bash-4.2#
```