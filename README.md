# docker-compose-basic-example

This is a basic example for Docker Compose that shows how to test and deploy a small architecture with multiple micro-services.


## Resources

The example in this repo is derived from the following resources.

### Setup instructions for Docker on Ubuntu Xenial64

https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-using-the-repository

### Setup instructions for Docker Compose

https://docs.docker.com/compose/install/#uninstallation

### Getting started with Docker Compose

https://docs.docker.com/compose/gettingstarted/#prerequisites

### Deploy on Azure

https://github.com/toddkitta/azure-content/blob/master/articles/virtual-machines/virtual-machines-docker-compose-quickstart.md

https://docs.microsoft.com/en-us/azure/virtual-machines/linux/docker-compose-quickstart


## To run and test on dev work station

Have Vagrant and VirtualBox installed.

Start the vagrant VM:

    cd docker-compose-basic-example
    vagrant up

Shell into the vagrant VM:

    vagrant ssh

Now you need to install docker and docker compose as shown in tutorial linked from the Resources section above.

Once in the VM change to the shared directory:

    cd /vagrant

Run the Docker Compose setup:

    sudo docker-compose up -d

Check that it's running:

    sudo docker-compose ps

Navigate browser on host PC to:

    http://localhost:5000

## Deploy to Azure

todo: 


## Issues

The setup when pretty much according to the tutorials with the exception of the following error when I tried to do 'docker-compose up' to boot the system.

    ERROR: Couldn't connect to Docker daemon at http+docker://localhost - is it running?

I had to use 'sudo docker-compose up' to bypass this issue. Seems to be related to using Vagrant.
