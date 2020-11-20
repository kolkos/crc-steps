# Installation
Installation Steps for Red Hat CRC


## Prerequisites 
Make sure you have the following:
* Red Hat account
* Log in to your redhat account: [Red Hat](https://cloud.redhat.com/openshift/install/crc/installer-provisioned)


## Installing CRC
Create a folder in your home dir

```
mkdir ~/crc
```

Open this folder

```
cd ~/crc
```

Download the CRC package

```
wget https://mirror.openshift.com/pub/openshift-v4/clients/crc/latest/crc-linux-amd64.tar.xz
```

Extract the tar
```
tar -xvf crc-linux-amd64.tar.xz
```

Move the binary file
```
sudo cp crc-linux-<version>-amd64/crc /usr/local/bin/crc
```

Clean your home dir
```
cd ~
rm -rf crc
```

## Test the installation
Run the following command and check if you get a respone:

```
crc version

# you should be getting something like this:
CodeReady Containers version: 1.18.0+bb304aa
OpenShift version: 4.6.1 (embedded in binary)
```


## Configuring CRC
Increase the ammount of memory that CRC may use
```
# For example 20GB (I have 32GB RAM Available)
crc config memory 20480
```

Make sure you do not use all of your ram.

## Run CRC Setup
This step is straight forward, just run the command:

```
crc setup
```

This will take some time. 

### Start and enable libvirt
For some reason my libvirt deamon has some issues, I have to run the following command every time after the setup command
```
sudo systemctl start libvirtd
```

I have tried to enable libvirt without any succes.

## Download the pull secret
On the following page, you could download the pull secret. 
[https://cloud.redhat.com/openshift/install/crc/installer-provisioned](https://cloud.redhat.com/openshift/install/crc/installer-provisioned)

Download the secret, move it to the root of your home dir:
```
move ~/Downloads/pull-secret ~/.
```


## Start CRC
Run the following command to run CRC for the first time
```
crc start -p ~/pull-secret
```

CRC will download a large package of files, so now is a good time to get some coffee. 

