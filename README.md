# Docker concepts  

## Advantage of docker

* Runs in same environment (works in one environment, works in all)
* Starts up very quickly
* Use fewer resources taking up less disk space

## Difference between docker and VM

* VM: each VM gets it's own full OS including the kernel (core of OS).
This is resource heavy
* Docker: Each container will use the host kernel and is shared across all 
containers


## Terms

* **Container**: Running instance of a image
* **Image**: Template for creating the environment you want. This will define the
OS, runtime, and application code all bundled up
* **Dockerfile**: How images are defined

