# VM Import into AWS EC2

A guide for importing a pre-built Virtual Machine (VM) and creating an Amazon Machine Images (AMI) based upon the imported VM.

## Steps

- Create a local VM using you desired hyperviser program and the OS ISO. This tutorial used VirtualBox version 6.0 and [Ubuntu 16.04.5 (Xenial Xerus)](http://releases.ubuntu.com/16.04/)
- Install SSH in your VM if it is not already installed

  `$ sudo apt-get install openssh-server`

- Use your hypervisor program to export VM as a single file (e.g. Open Virtual Appliance (OVA) format)
- Refer to [this](https://docs.aws.amazon.com/vm-import/latest/userguide/vmimport-image-import.html) documentation and upload you OVA file into Amazon S3 and also create an IAM role named vmimport and finally import your VM. Please note that uploading you OVA and also importing the VM might take up to 1 hours each
- After the import is completed, go to EC2 Dashboard->Launch Instance->My AMIs and create an instance using your imported VM
- SSH into your instance and code on!
