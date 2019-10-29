# watcher
A subdomain enumeration script written in Bash. It uses common API's to extract subdomains quickly (webarchive, crt.sh etc.). It may be also used with prepared docker images of other popular subdomain enumeration tools.

Installation:
        
    apt -y install docker.io

Usage:
    
    ./watcher domain.com


!Dockers!
The script comes with commands that pull docker images of known subdomain enumeration tools and runs them on the target (in addition to other used techniques). If time is a concern - simply comment-out the docker sections.

You may take inspiration from this and add any other docker-based tool that you need. to use:

1. go to the "tools deployment" section and copy any tool's template
2. to easily search for a prepared image, use "docker search xyz"
3. if your docker image only takes an IP as a target, do as follows:

     docker run johnpaulada/ctfr -d $(resolveip -s $target) | tee -a $c
