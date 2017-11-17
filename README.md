# Building dependency packages for Lambda

<div class="3D&quot;Section1&quot;">

When building a Lambda function it is sometimes necessary to pre build the Python and Nodejs modules using Amazon Linux.

This can either be done remotely on an EC2 = instance or locally in a Docker container.

## Creating an Amazon Linux Docker container

Clone repo in to local directory.
<pre>git clone https://github.com/andrewmooney/Lambda-Dockerfile.git</pre>

In a terminal window navigate to the location of the Dockerfile and run the following command.
<pre>docker build --no-cache -t amazonlinux-lambda -f Dockerfile .</pre>

Once the build has completed run the follow= ing command to launch the container.
<pre>docker run -it amazonlinux-lambda</pre>

This should drop you in to the shell of the container.
<pre>bash-4.2#</pre>