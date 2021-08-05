# Cloud_Foundry_Bosh
build cloud_foundry in legancy HP Z600 workstation using BOSH

## Prerequisites(Hardware and main software tools)
- 1. HP Z600 workstation: CPU: Intel(R) Xeon(R) E5620 @2.40GHz,Mem:9.7Gi, HHD storage: 500GB
- 2. OS: Ubuntu server 20.04 uname: Linux z600 5.4.0-80-generic #90-Ubuntu SMP Fri Jul 9 22:49:44 UTC 2021 x86_64 x86_64 x86_64 GNU/Linux
- 3. Install the [bosh CLI](https://bosh.io/docs/cli-v2-install/) and its [additional dependencies](https://bosh.io/docs/cli-v2-install/#additional-dependencies).
- 4. Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

## Install 

- First, create a workspace for our virtualbox environment.
'''  
  mkdir -p ~/bosh-env/virtualbox
  cd ~/bosh-env/virtualbox
'''
- Next, we'll use bosh-deployment, the recommended installation method, to bootstrap our director.
'''
  git clone https://github.com/cloudfoundry/bosh-deployment.git
'''
- Now, we can run the virtualbox/create-env.sh script to create our test director and configure the environment with some defaults.
'''
  ./bosh-deployment/virtualbox/create-env.sh
'''
