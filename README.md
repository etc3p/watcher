# watcher
A subdomain enumeration script written in Bash. It uses common API's to extract subdomains quickly (webarchive, crt.sh etc.). It may be also used with prepared docker images of other popular subdomain enumeration tools.

Usage:
    
    ./watcher domain.com



!Dockers!

The script comes with two commented-out parts that pull docker images of known subdomain enumeration tools and runs them on the target (in addition to other used techniques). These come commented-out by default due to time consumption.

You may take inspiration from this and add any other docker-based tool that you need. to use:

1. apt -y install docker.io
2. comment-out or add your own images based on the templates
3. to easily search for a prepared image, use "docker search xyz"
4. If your docker image only takes an IP as a target, do as follows:

     docker run johnpaulada/ctfr -d $(resolveip -s $target) | tee -a $c
